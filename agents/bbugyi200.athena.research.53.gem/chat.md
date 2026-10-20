# Chat History - ace-run (research.53.gem)

- **TIMESTAMP:** 2026-10-20 07:04:32 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.53.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261020_065153.md`

## Prompt

%id(gem, clan=research.53)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.53.cdx`, `research.53.cld`, `research.53.grk`, `research.53.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add support for directed links from one Obsidian task to another.

- I was thinking that we could display these links via a new `LINKS` task sub-bullet or
  somethiing like that.
- Tasks should also track their backlinks (via a new `BACKLINKS` sub-bullet?), which
  must always stay consistent and correct (i.e. this field needs to be kept up-to-date
  automatically somehow).
- I need to be able to easily specify links when capturing new tasks in the
  bob-mac-capture app. I was thinking I could use a new `~` syntax for that which
  triggers a completion menu / search interfact for other Obsidian tasks (which we will
  link the current task to).
- We also need a way to specify that another task should link to the current task in
  both Obsidian (via the `<ctrl+shift+p>` keymap?) and in the bob-mac-capture app (via a
  new `~~` syntax maybe?).
- The user should be able to specify an optional relation / link description when adding
  a link from one task to another.
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

# Research Report: Directed Task Links and Backlinks

**Report File:** [`directed_task_links__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/directed_task_links__gem.md)  
**Registered Artifact:** `research:202610/directed_task_links__gem.md` (`file:explicit:39befded9fd333bebc07b5e6`)  
**Researcher:** `research.53.gem`

---

## Executive Summary & Bottom Line

**Build directed task links, but reject physical `BACKLINKS` markdown lines and the `~~` capture syntax.**

The user's intuition solves a genuine deficiency in the Bob ecosystem. Currently, Bob only supports hard execution dependencies (`⛓️ **DEPENDS ON:**` / `🧱 **BLOCKS:**`). When tasks are conceptually related but do not block each other, putting them in `DEPENDS ON` breaks the workflow: tasks become `[?] Blocked`, get excluded from the Ready queue, get consumed and removed from active Pomodoros, and distort GTD review walks. Conversely, dumping links in unstructured markdown notes loses structured querying, bidirectional discovery, and fast capture.

However, two specific mechanisms in the initial plan are architecturally hazardous:
1. **Physical `BACKLINKS` lines cause severe write amplification and sync conflicts.** Writing a physical line under target tasks across the vault turns a single capture in `inbox.md` into a multi-file write cascading into `projects/`, `areas/`, or even immutable archives in `done/`. In a multi-device setup (Syncthing/iCloud), this triggers sync collisions and git churn. **Backlinks must be virtual projections**, rendered dynamically in Obsidian from the link cache and queried on demand in the CLI.
2. **The `~~` capture syntax collides with CommonMark strikethrough.** In Markdown, `~~text~~` is strikethrough. In Bob's codebase, `~~[[#^id]]~~` is already parsed as a struck (completed) link. Using `~~` introduces severe lexical ambiguity. Reverse linking should instead be driven by an interactive direction toggle in the macOS capture picker (or an explicit non-colliding sigil like `~^`).

---

## Core Critique & Requirement Adjustments

### The Critique
- **Is this a good idea?** Yes, conceptually. Establishing soft associative links between tasks (subtask, split-from, relates-to) completes the triad of task modeling alongside hard dependencies and freeform prose.
- **Where the plan fails:**
  - *Physical Backlinks:* High write amplification, dirty git trees across unrelated notes, sync conflicts, and archive pollution.
  - *`~~` Syntax:* CommonMark strikethrough collision.
  - *Directional Ontology:* Unstructured descriptions lack natural language inverses (e.g. `parent of` needs to invert to `subtask of` on the target).

### Key Requirement Adjustments
- **[ADJ-1] Forward Links on Managed Line:** Store links authoritatively on `- 🔗 **LINKS:** [[target#^id]] (relation) • …` directly under the `#task` bullet, following Bob's established child line conventions (`docs/task-dependencies.md` §2.4).
- **[ADJ-2] Virtual Dynamic Backlinks:** Do not write physical `BACKLINKS` lines. In Obsidian, `bob-ledger-tools` dynamically computes and renders live inbound chips from Obsidian's `metadataCache`. In the CLI, `bob task links --inbound <target>` queries them instantly.
- **[ADJ-3] Capture Sigils & Rejection of `~~`:** Use `~note:block-id(relation)` for forward links. Replace `~~` with a direction toggle in the macOS capture picker (`Tab` or `Cmd+R`), or an explicit prefix `~^note:block-id`.
- **[ADJ-4] Structured Relation Syntax:** Encode relations as trailing parentheses: `[[note#^id]] (relation)` (or omit for default `relates`).
- **[ADJ-5] Curated Ontology with Inverse Mappings:** Support paired relations (`parent` $\leftrightarrow$ `subtask`, `split-from` $\leftrightarrow$ `split-to`, `causes` $\leftrightarrow$ `caused-by`, `relates`) while permitting freeform strings.
- **[ADJ-6] Strict Execution Isolation:** General links never alter task status, never trigger Pomodoro promotion, never consume live Pomodoro links, and never modify GTD lanes.
- **[ADJ-7] Task Card Keymaps:** In Obsidian, `Ctrl+Shift+P` opens the Task Card: press `l` for the Links stage, `⇧L` for Linked By. Direct hotkeys: `Ctrl+Shift+L` / `Ctrl+Shift+Alt+L`.
- **[ADJ-8] Rich Status Chips:** In Obsidian Live Preview and Reading View, transform raw links into status-tinted pill chips with status glyphs, relation badges, hover removal (`×`), and an add (`＋`) button.

---

## Architecture Overview

```
                                      ┌──────────────────────────────────────────────┐
                                      │              bob-mac-capture                 │
                                      │  - Types: ~target:id(subtask)                │
                                      │  - Tab to toggle direction (Links vs By)    │
                                      │  - Quick-select relation (1:relates, 2:sub)  │
                                      └──────────────────────┬───────────────────────┘
                                                             │
                                                  Spawns bob capture-parse
                                                  & bob capture
                                                             │
                                                             ▼
┌──────────────────────────────────────────────┐     ┌───────────────────────────────────────┐
│              bob-plugins (Obsidian)          │     │               bob-cli                 │
│  bob-navigation-hotkeys:                     │     │  src/native/task_links/:              │
│  - Task Card 'l' & '⇧L'                      │     │  - Scanner, parser, formatter         │
│  - Ctrl+Shift+L / Ctrl+Shift+Alt+L           │◄────┤  src/native/capture_language/:        │
│  - Vault-wide Links Stage modal              │     │  - ~ sigil & (relation) parsing       │
│                                              │     │  src/native/task_status_hooks/:       │
│  bob-ledger-tools:                           │     │  - reconcile_links pass               │
│  - Live Preview & Reading View chips         │     │  - Link healing on task move          │
│  - Virtual Backlinks resolver & popover      │     │  - Empty line pruning                 │
└──────────────────────────────────────────────┘     └───────────────────────────────────────┘
```

---

## Artifact & Snapshot Registration

The comprehensive research report has been written and permanently registered in the research repository:
- **Absolute Path:** `/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/directed_task_links__gem.md`
- **Artifact Ref:** `file:explicit:39befded9fd333bebc07b5e6` (`research:202610/directed_task_links__gem.md`)
- **Final Declaration:** Submitted and accepted for repository `sdd:research` commit.
