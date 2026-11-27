# Chat History - ace-run (1h6--plan)

- **TIMESTAMP:** 2026-11-27 10:38:45 EST
- **MODEL:** claude/opus
- **AGENT:** 1h6--plan

**Plan:** /home/bryan/.sase/plans/202611/property_card_equals_keymap.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/property_card_equals_keymap.md`

> # Move the Property Card editor gesture from `==` to `=`
> ## Goal
> In Live Preview Vim normal mode, a bare `=` opens the current note's Property Card
> editor (the "species editor": album schema card, Bank Setup, Record Card, Area/Project
> Settings, Intention Card editor, Notebook/Prose focus-or-add, the Reference editor) on
> every note where `==` does today. `==` stops being the gesture. Every hint, wire value,
> doc, and glossary entry that teaches `==` for this gesture says `=` afterwards. Nothing
> else about `-`, `_`, or `+` changes.
> ## Verified: `=` is free as a normal-mode prefix
> Planning checked every place a bare normal-mode `=` could already be claimed:

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me migrate the `==` keymap, which triggers the current file's
property card schema editor, to `=`? We don't use `=` as the prefix for any other
keymaps at the moment, so I think this should be safe (you should verify).

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

Looking into where the `==` keymap is defined. It sits in the bob-plugins property-card kit, so I'm opening that repo next.

Now the memory-write skill, since nine glossary strands describe the gesture as `==`.

Research is done. `=` is free as a prefix: the vault vimrc, `hotkeys.json` (only Ctrl+=), and the plugin Vim maps don't use it. Writing the plan now.

Now updating the body callouts and references to match the toggle decisions.

Validation passes. One last read of the full plan for coherence before proposing.

The proposal is staged. Finishing the turn through `/sase_final`.

I've written and proposed a plan to move the card editor gesture from `==` to `=`; no code has changed yet, and it's waiting for your approval. It passed `sase plan validate`. It's a single-agent plan of medium size, covering bob-plugins and bob-cli.

**`=` is free to take.** Nothing else starts with `=` in normal mode:
- **Your vimrc** (`obsidian_vimrc.md`) maps nothing starting with `=`.
- **`hotkeys.json`** only uses Ctrl+=, and the gate ignores modified keys.
- **Plugin Vim mappings** don't use `=` in any plugin.
- **The only key listener for `=`** in the editor is the one that handles `==` today. Other `=` handlers only run inside a card editor once it's open.
- **Capture's `=` and `==`** (the relation alias and the Pomodoro override) are typed-text syntax, not keymaps, so they stay as they are.

**What you give up:** Vim's `=` reindent, but only on notes that have a card. On every other note `=` behaves as stock Vim. Counted `N==`, register prefixes, visual and insert modes, Source mode, and prefixed keys like `f=` and `r=` also keep Vim's behaviour.

**What changes:**
- **bob-plugins:** a single `=` opens the editor directly. The on-screen hints, tests and docs switch to `=`, and the `[n==r` / `==[r` shortcuts become `[n=r` / `=[r`.
- **bob-cli:** `bob props` reports `editor: "="` instead of `"=="`. That changes the JSON output, so the commit is marked as a breaking change (`feat(props)!`). The plugin ignores this value, so the two repos can ship in either order.
- **bob-cli docs:** the period-note callout text and the props and periods docs switch to `=`, and the generated glossary page is rebuilt.

**Decisions for you at approval:**
1. **Swallow a quick second `=`** (on by default): a second `=` pressed within 350 ms of the first is ignored. Every card editor uses `=` itself, so without this the old `==` habit would also trigger it. For example, the Record Card would jump to the album schema.
2. **Bump the period callouts to v4** (off by default): this would let `bob periods ensure -R` rewrite the 59 existing period notes that say "`==`, then `r`". Leaving it off means only new notes say `=`, which avoids flagging every period note as stale over a key hint.
3. **Update the nine glossary entries** for the card types (on by default): they currently describe the gesture as `==`, which would become false.
