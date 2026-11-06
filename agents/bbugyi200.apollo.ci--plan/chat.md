# Chat History - ace-run (ci--plan)

- **TIMESTAMP:** 2026-11-04 18:35:06 EST
- **MODEL:** claude/opus
- **AGENT:** ci--plan

**Plan:** /home/bryan/.sase/plans/202611/mac_capture_word_motions.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/mac_capture_word_motions.md`

> # Plan: Vim-style word motions in the Bob Mac Capture editor
> ## Goal
> In the Bob Mac Capture draft editor (the main capture input box), add four caret motions
> that work like vim's word motions:
> | Key          | Vim motion | Moves the caret to                                 |
> | ------------ | ---------- | -------------------------------------------------- |
> | Ctrl-L       | `W`        | start of the next WORD (run of non-blank chars)    |
> | Ctrl-H       | `B`        | start of the current or previous WORD              |
> | Ctrl-Shift-L | `w`        | start of the next word (keyword / punctuation run) |
> | Ctrl-Shift-H | `b`        | start of the current or previous word              |

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Can you help me add the `<ctrl+h>` and `<ctrl+l>` keymaps to the
bob-mac-capture app that act like the `B` and `W` keymaps in vim's normal mode,
respectively?

- In other words, I want to use these keymaps to jump to the previous and next word in
  the capture input box (where a "word" is any sequence of non-whitespace characters I
  think, or something like that--do what vim does).
- Let's also add the `<ctrl+shift+h>` and `<ctrl+shift+l>` keymaps that act like the `b`
  and `w` keymaps in vim, respectively.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

## Response

I'm exploring bob-mac-capture's key routing so I can plan the Ctrl+H/L (and Ctrl+Shift+H/L) word-motion keymaps.

Still exploring: I've found the key router and the Ctrl-A/E and Ctrl-Shift-J/K motion helpers; now I'm checking existing Ctrl+H/L uses, tests, and the keymap docs.

Now let me look at the existing router tests and how the controller dispatches keys (marked text, similar-row focus, the verticalMovementGoal reset).

I've mapped the router, controller, test harnesses, and docs; now checking global-hotkey defaults for Ctrl+H/L conflicts, then I'll write the plan.

Nearly done exploring — verifying how the prompt branches treat Ctrl-H/L so the docs table rows are accurate, then writing the plan.

I have what I need. Writing the plan now.

Let me verify one test expectation (editor-leader handling of Ctrl-L) before validating.

Confirmed. Now validating the plan.

The plan validates. Submitting it.

I've written and submitted a plan for the four word-motion keymaps. It's waiting for your approval, and no code has changed yet. It's a single-agent plan sized `medium`, and all the work happens in the `bob-mac-capture` repo.

**Keys** (they work only in the main capture input box):

| Key | Vim | Moves to |
| --- | --- | --- |
| Ctrl-L | `W` | start of the next WORD (any run of non-whitespace) |
| Ctrl-H | `B` | start of the current or previous WORD |
| Ctrl-Shift-L | `w` | start of the next word (letters/digits/`_` run, or a punctuation run) |
| Ctrl-Shift-H | `b` | start of the current or previous word |

For example, `@foo#bar` is one WORD but four words: `@`, `foo`, `#`, `bar`.

**How it behaves:**
- **Vim rules:** the motion logic copies vim's own word-motion code. Blank lines count as words; lines that contain only spaces don't. Emoji count as their own kind of word, and Chinese, Japanese and Korean text splits by script, as in vim.
- **One difference from vim:** pressing Ctrl-L on the last word moves the caret to the end of the draft. In normal mode vim stops on the last character, but the capture box behaves like insert mode.
- **Start and end of the draft:** the motion stops there and doesn't wrap. The key is still swallowed, so Ctrl-H never falls through to macOS's built-in "delete backward" binding and deletes a character. Inside the input box, Ctrl-H will no longer delete; Backspace and Ctrl-U still do.
- **Selected text:** the selection collapses, like Option-Arrow. Forward motions start from its end, backward motions from its start.
- **Other keys stay as they are:** the relation-label card keeps its Ctrl-H "show hidden" toggle, and the pickers, other prompts and the Ctrl-G leader key keep their own handling. If the suggestions list is open, it stays open. While you're composing text with an input method (e.g. Japanese input), the keys go to it.

**What the plan builds:**
- The motion logic goes in the shared core module, so it can be tested on Linux. The plan includes a table of expected caret positions I traced by hand.
- Small additions to the key router and panel controller, with tests for each.
- New rows and a short explanation in `docs/keyboard.md`.

**Compile checks:** Swift isn't installed on apollo, so the plan has the implementer:
- run `just portable-check` on athena;
- compile the Mac app on the Mac if it's online, or say in the report that the macOS targets weren't verified if it isn't;
- run `just docs-check`.

**Left out:** counts like `3w`, the `e`/`ge` motions, and word motions inside picker filters and one-line prompts.
