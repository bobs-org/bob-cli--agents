# Chat History - ace-run

- **TIMESTAMP:** 2026-07-09 12:42:50 EDT
- **MODEL:** claude/opus
- **AGENT:** research.5.cld
- **PROMPT:** `~/.sase/multi_prompts/202607/gh_bobs_org__bob_cli-multiprompt-260709_123941.md`

## Prompt

%name:research.@.cld %m:@research_assist %g:research #gh:gh_bobs-org__bob-cli There are 3 Obsidian tasks queries in the ~/bob/dash.md file that are nearly identical. It would be great if we could de-duplicate them somehow using some shared tasks query functionality of some sort. Can you do some research to help me understand what options I have available to solve this problem? End your analysis with a recommended solution. Write this research to a new markdown file under the $(sase sdd path research)/$(date +%Y%m)/ directory.


## Response

I'll research this. Let me start by reviewing the relevant context: the Obsidian memory, the actual `dash.md` queries, and any prior research on this topic.

Let me read the existing (committed) research on this exact topic, check the installed Tasks plugin version in the vault, and verify current plugin features.

A thorough, committed research file on this exact topic already exists at `sdd/research/202607/dedupe_dash_tasks_queries.md` (from a prior agent, `research.4.cld`). Its local-environment claims verify against what I'm seeing now (Tasks v8.0.0, presets in active use, empty `globalQuery`). I'll independently verify the external claims before writing a fresh doc to your requested `.sase/...` location. Let me load web tools.

I'll verify the Presets feature (syntax + version) and Global Query override semantics against the official Tasks docs.

All external claims verify against the official Tasks docs:
- **Presets** introduced in Tasks **7.20.0**; syntax `preset <name>` (statement) and `{{preset.<name>}}` (placeholder, usable inside Boolean combos); "applied exactly as written and cannot be modified" (no parameters); can nest and combine. ✓
- **Global Query** prepends to *all* queries; opt-out is all-or-nothing via `ignore global query`; "It isn't always possible to override a filter set in the Global Query" (issue #2074). ✓

Now let me create the target directory and write the research file.

Done. I researched the options and wrote the analysis to:

`.sase/sdd/research/202607/dedupe_dash_tasks_queries.md`

## What I found

Your three blocks in `~/bob/dash.md` (WIP / NEXT / READY) are identical except for **one line** — the status selector. The other ten lines (folder filter, `is not blocked`, the scheduled/`#hide` function filters, grouping, sorting, `short mode`, `hide toolbar`) are copy-pasted three times.

I evaluated five options and verified every claim against both the live vault and the official Tasks docs:

| Option | Verdict |
|---|---|
| **1. Tasks Presets** | ✅ **Recommended** |
| 2. Global Query | ❌ Wrong scope — hits all 14 daily-note queries too, opt-out is all-or-nothing |
| 3. Templater | ❌ Only DRY at generation time; file on disk still has 3 expanded blocks |
| 4. dataviewjs / Tasks API | ❌ Loses native Tasks status semantics + toolbar; most fragile |
| 5. Do nothing | ❌ Keeps the three-way manual edit cost |

## Recommendation: Tasks **Presets**

Define one preset (`dash_common`) holding the ten shared lines, then each block shrinks to two lines — its status filter plus `preset dash_common`. It's the purpose-built, first-party feature for exactly this; each block stays a genuine live query with all behavior intact. The file includes the exact preset definition (both settings-pane and `data.json` forms) and the rewritten blocks.

**Why Presets fits especially well here:** your vault is already on Tasks **v8.0.0** with Presets in active use (the stock `hide_everything` preset already nests others, `this_file` already uses placeholders), `globalQuery` is empty, and since presets are plain JSON in `data.json` they're editable through your headless `ob` workflow — not GUI-only.

## One thing to flag

A near-identical research note **already exists in the repo** at `sdd/research/202607/dedupe_dash_tasks_queries.md` (committed as `251469b` by a prior agent). It reaches the same conclusion. I re-verified its claims rather than trusting them blindly — they hold up — and noted the overlap in a "Related prior work" section of the new file. If you didn't intend a second copy, you may want to keep one and drop the other; the older one lives under `sdd/`, the new one under `.sase/sdd/` as you requested.

I did **not** modify `dash.md` or the plugin settings — this is research only. Say the word if you'd like me to apply the change.
