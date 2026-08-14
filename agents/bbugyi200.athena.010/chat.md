# Chat History - ace-run (010)

- **TIMESTAMP:** 2026-08-14 09:27:51 EDT
- **MODEL:** grok/grok-4.6
- **AGENT:** 010

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me review the most recent epic bead worked for this project and highlight its benefits? %m:grok-4.6

## Response

I'll look up how SASE beads work, then find this project's most recent epic and review what it delivered.

Next I’ll read the bead rules and look up this project’s recent epic work.

The latest epic is in progress: Native Bob Mac Capture. I’ll pull the plan, phases, and what’s landed so I can review it and call out the benefits.

The epic is closed with all seven phases done. Next I’ll read the plan, phase notes, and follow-ups so the review is grounded in what actually shipped.

I have the plan and land notes. I’ll spot-check the shipped CLI contracts and the Mac app so the benefits are based on what actually landed.

The most recent epic for this project is **`bob-cli-j`: Native Bob Mac Capture app**. It was created and closed **done** today (2026-08-14): seven phases, land-verified, and already in daily use as the replacement for the Hammerspoon capture pop-up.

- Bead: [bob-cli-j](https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-j/README.md)
- Plan: `plan:202608/bob_mac_capture.md`
- Goal: a signed native macOS 26 menu-bar app in `bobs-org/bob-mac-capture` that owns the UI, while **bob-cli remains the only implementation of capture grammar and vault writes**

---

## What it replaced

Capture used to live in Hammerspoon: a WebView pop-up plus a **second copy of the capture grammar in Lua** (`task_capture.lua`). That stack could not do real multi-line editing well, could disagree with `bob capture`, and mixed UI, parsing, and vault mutation across two languages.

The epic deleted that duplicated grammar and the WebView workflow from chezmoi, and moved the panel to a native `LSUIElement` app. Rollback is documented (chezmoi `3d841c1e` plus the app’s Control-Shift-Command-O preference).

---

## Benefits

### 1. Capture now feels like a real Mac app

The panel is a **pre-warmed, non-activating native editor**, not a WebView that is built on the hotkey. That is why the plan could set a hotkey-to-focus budget of p50 &lt; 50 ms / p95 &lt; 100 ms: panel construction and `bob` discovery are off the hotkey path.

Day-to-day that means:

- Multi-line drafting (Return submits; Shift/Option-Return inserts a newline; Command-Return submits and opens the note)
- Escape keeps a nonempty draft instead of throwing it away
- A menu-bar app with Settings, launch-at-login, and a documented production hotkey (Control-Shift-Command-I)
- No Accessibility permission (Carbon `RegisterEventHotKey`, not an event tap)

Post-ship usage already produced polish on this surface (auto-dismiss after success, restore-after-launch, completion dismiss). The app is not a scaffold sitting unused.

### 2. Highlighting, completion, and preview cannot drift from `bob`

This is the architectural win, and it is why the first two phases were in **bob-cli**, not Swift.

| New command | What the app gets | Why it matters |
|---|---|---|
| `bob capture-parse` | Spans, mode, diagnostics | Marker coloring comes from the same tokenizer `bob capture` uses |
| `bob capture-complete` | Cursor-aware candidates + replacement ranges | The app never invents `@route`, `#section`, `^task`, or `:pomodoro` syntax |
| `bob capture --dry-run --no-clip` | Exact destination and rendered Markdown | Live preview is the write, not a Swift approximation |

Concrete payoffs:

- Incomplete markers (`@`, `@cash^`, `@route#`) are valid **editor** states, not fatal CLI errors
- Live preview **never reads the clipboard**, so typing `%` / `%N` / `%header` does not leak or mutate Clipy history; only explicit Preview or Capture resolves them
- A `p:<N>` roll is seeded once per draft (`BOB_PRIORITY_ROLL_SEED`) so the date you see is the date that gets written
- Cached route completions stay fast; FSEvents refreshes the vault without blocking typing

The Lua grammar is gone. There is one capture language.

### 3. Failed captures are lossless

The old implicit failure mode — lose the draft, or silently dump into inbox — is gone.

- One in-flight submit; repeated Return cannot double-write
- Any failure (missing route, bad JSON, missing `bob`, timeout) keeps the **full draft and last destination** on screen
- Inline error + Copy Diagnostic; notifications are extra, not required for correctness
- Every `bob` call is a direct `Process` argv array with a 20s timeout, never `/bin/zsh -lc`
- Notification bodies omit captured text; diagnostics and signposts are metadata-only

That is a reliability and privacy upgrade, not just a prettier panel.

### 4. bob-cli got two reusable editor APIs

Even without the Mac app, `capture-parse` and `capture-complete` are versioned, documented, Linux-tested contracts (shared `src/native/capture_language.rs`). Any future editor — another frontend, a TUI, tests — can highlight and complete against the same grammar. Hammerspoon could not offer that without reimplementing Lua again.

### 5. Install, CI, and rollback are first-class

The epic treated shipping as part of the product:

- Stable bundle id `org.bobs.bob-mac-capture`, signed install, atomic `install.sh` with backup-and-swap
- macOS 26 CI: format, build, test, bundle, `plutil`, codesign, plus a launch-complete signpost so a silent empty AppKit process fails CI
- Settings surfaces bob path, vault, hotkey conflicts, notification authorization, and signing state
- Chezmoi cutover is reversible without running two production hotkeys at once

---

## What the review would not oversell

The land agent was explicit: **every physical-Mac checklist item is still unrun**. Agents on this epic ran on Linux `athena`. Formal latency, IME, VoiceOver, Spaces, multi-display, and secure-input measurements were never recorded. That work is already filed as ready task **`bob-cli-k`**.

Two smaller leftovers, not regressions of the product idea:

- **`bob-cli-c`** (reopened): Pomodoro block-ID error text still claims `_` is legal; the parser rejects it
- **`bob-cli-l`**: retired SASE agent-hood publication requests that muddy commit links in `bob-mac-capture`

Land also had to fix an epic-owned test crash (`AppDelegate` eagerly constructing `NotificationService` outside an app bundle) so macOS CI is green at `f59ab74`. That is the kind of hardening you expect from a first native AppKit app, and it was integrated before close.

---

## Bottom line

`bob-cli-j` is the biggest product change in this project’s epic history: capture moved from a Hammerspoon WebView with a shadow Lua grammar to a native, signed menu-bar app driven entirely by bob-cli. The benefits you actually feel are **speed, multi-line editing, draft safety, and preview/completion that cannot lie**. The benefit you will keep feeling is **one grammar**: future capture features only have to land in Rust, and the Mac UI consumes them.

The remaining value is sitting in **`bob-cli-k`** — run the owner-assisted on-Mac gate so the latency and accessibility claims are measured, not just designed.
