# Chat History - ace-run (research.27.gem)

- **TIMESTAMP:** 2026-10-20 16:04:54 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.27.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261020_155257.md`

## Prompt

%id(gem, clan=research.27)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.27.cdx`, `research.27.cld`, `research.27.grk`, `research.27.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would love to be able to start showing likely related tasks in the bob-mac-capture
app's preview panel when the capture the user has input will result in one or more new
tasks being created.

- The main benefit of this feature would be that it gives the user a heads up about
  duplicate tasks and/or related tasks that they might want to link to in some way.
- The biggest concern here is performance. The bob-mac-capture app must remain blazing
  fast.
- A secondary concern would be how we fit all of this in the panel without making it too
  cramped or making the user need to scroll too often.
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

# Research Report: Real-Time Related & Duplicate Task Preview in Bob Mac Capture

The comprehensive research report has been completed, written to disk, and registered as a durable SASE artifact:

- **Report Path:** [`mac_capture_related_tasks_preview__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22/sase/repos/research/202610/mac_capture_related_tasks_preview__gem.md)
- **Artifact Label:** `research:202610/mac_capture_related_tasks_preview__gem.md`
- **Artifact ID:** `explicit:b05d005959a30e7cdd648c09`

---

## Executive Summary & Plan Critique

### 1. Is this a good idea?
**Yes, but only if designed as an ambient, non-blocking superpower rather than a noisy, mandatory triage step.**

In GTD and PKM workflows, duplicate tasks and fragmented contexts are persistent pain points. Catching duplicates at capture time prevents vault rot. Surfacing related tasks allows immediate dependency wiring.

However, a naive implementation introduces three severe hazards:
1. **Keystroke Latency & Battery Drain:** [`bob capture --dry-run`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22/src/native/capture/cli.rs) currently executes in **~5 ms** because it only reads the single note targeted for insertion (e.g. `mac_inbox.md`). Running a full vault scan (hundreds of Markdown files) on every keystroke debounce would surge latency to **50–250 ms**, causing typing stutter and draining battery.
2. **Disrupting the Capture Mindset:** The primary purpose of [`bob-mac-capture`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/CapturePanelView.swift) is low-friction, rapid brain-dumping. Intrusive task cards jumping into view create friction and "banner blindness."
3. **Panel Height & Layout Jitter:** Injected task blocks will blow past the 720pt screen cap, engage the auxiliary `ScrollView`, and violate the panel's steady-height policy.

---

## Key Adjustments to the Requirements

1. **Strict Task-Creation Classification:**  
   Only evaluate related tasks when the parsed draft *definitely results in one or more new tasks being created* ([`CaptureKind::Task`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22/src/native/capture_language/model.rs), [`CaptureKind::TaskWithBlockId`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22/src/native/capture_language/model.rs), [`CaptureKind::Pomodoro`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22/src/native/capture_language/model.rs) with new task body, or [`CaptureKind::ProjectNote`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22/src/native/capture_language/model.rs)). Never run for session operators (`=`, `x`), duration adjustments (`+5`), completions (`!`), reference URLs, or existing task links (`^`, `@:`).
2. **Content Length & Significance Gate:**  
   Require $\ge 4$ characters and at least one non-stopword token (filtering standalone verbs like *fix, check, update, do*).
3. **Two-Tier Match Handling:**  
   - **High-Confidence Duplicate (Score $\ge 0.85$):** Prominent amber warning pill (`⚠️ Duplicate found in errands.md ^a1b2`) with single-keystroke conversion.
   - **Contextually Related Tasks (Score $0.45 – 0.84$):** Discreet, calm 1-line chip (`[ 🔗 2 related tasks ]`), never auto-expanding.
4. **Decoupled In-Memory Architecture:**  
   Do not query the disk on keystrokes. [`bob-cli`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22/src/native/capture_tasks.rs) exports the open-task catalog, which [`bob-mac-capture`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22/sase/repos/linked/bob-mac-capture/Sources/CaptureCore/BlockIDPickerIndex.swift) caches in memory and revalidates via [`VaultTargetWatcher`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/VaultTargetWatcher.swift) (FSEvents). In-memory search in Swift runs in **$< 0.5\text{ ms}$**.

---

## Recommended Solution Architecture

### 1. Dual-Tier Performance Architecture
- **`bob capture-tasks --all --format json`:** Authoritative endpoint in `bob-cli` emitting all open vault tasks, locators, block IDs, and tags.
- **`CaptureTaskIndex` (Swift Actor):** Maintains precomputed `FuzzyField` boundaries and an inverted token index in memory (~250 KB footprint).
- **Zero Keystroke I/O:** Keystrokes query `CaptureTaskIndex` in RAM ($\approx 0.3\text{ ms}$), completely preserving the 5ms preview benchmark.

### 2. UI Presentation Ladder (Steady-Height Budget)
- **Tier 1 (Default / Calm):** Single 22pt accessory chip inside [`PreviewPane`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/CapturePanelView.swift#L2443):  
  `🔗 2 related tasks (⌥R to view) · top: staging ingress proxy (ops.md)`
- **Tier 2 (Duplicate Alert):** 36pt amber capsule banner:  
  `⚠️ Likely duplicate in errands.md ^c49a: "Order fridge water filter"`  
  `[⌥: Link Existing Today]  [⌥/ Open in Obsidian]  [⏎ Create Anyway]`
- **Tier 3 (Expanded Shelf):** Up to 3 compact comparison cards displayed only on explicit user request (`⌥R`, `Tab`, or click).

### 3. Single-Keystroke Splicing Superpowers
Users can act on related tasks without touching the mouse or memorizing syntax:
- `⌥:` $\rightarrow$ **Link Existing Today:** Replaces draft with `@note:block-id` to pull into today's Pomodoro.
- `⌥&` $\rightarrow$ **Make Prerequisite:** Appends `&note:block-id`.
- `⌥*` $\rightarrow$ **Make Blocker:** Appends `*note:block-id`.
- `⌥~` $\rightarrow$ **Relate Tasks:** Appends `~note:block-id`.
- `⌥+` $\rightarrow$ **Make Child Task:** Converts to sub-bullet under `+note:block-id`.

---

Please review the full report at [`mac_capture_related_tasks_preview__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22/sase/repos/research/202610/mac_capture_related_tasks_preview__gem.md) for complete algorithmic models, scoring weights, JSON contracts, and implementation phases.
