# Chat History - ace-run (research.3d.gem)

- **TIMESTAMP:** 2026-11-05 11:05:34 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.3d.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261105_104925.md`

## Prompt

%id(gem, clan=research.3d)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.3d.cdx`, `research.3d.cld`, `research.3d.grk`, `research.3d.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

we already have good support for Google Calendar (via the `bob gcal` command) and Google
Keep (via the `bob gkeep` command). I would like to now add a new `bob gmail` command
that we use to integrate Google Mail (bryanbugyi34@gmail.com) into my Obsidian vault.

- For example, when a capture contains a link like
  https://mail.google.com/mail/u/0/#inbox/FMfcgzQhWTsNRgxMhQNwhZDfgqwXpPsx, we should
  ideally be able to use this to:
  - fetch the email's contents
  - store it to a note file in my Obsidian vault that renders the email beautifully in
    Obsidian
  - link to that note file from the capture text using a link that replaces the URL and
    uses a good label (the email subject and/or sender?)
- It would also be great if I could write and send new emails directly from Obsidian
  somehow.
- If there are any other objectively useful features that fall out of this integration,
  you should recommend those as well.
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

# Research Report: `bob gmail` Vault Integration & Capture Protocol

**Report Location:** [`sase/repos/research/202611/bob_gmail_vault_integration__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_37/sase/repos/research/202611/bob_gmail_vault_integration__gem.md)  
**Durable Snapshot:** `research:202611/bob_gmail_vault_integration__gem.md` (`file:explicit:be81807b6c5d0a0b2a8d7db9`)  
**Researcher:** `research.3d.gem` (5-researcher swarm)

---

## Executive Summary & Core Verdict

- **Yes to email archival, vault rendering, and GTD inbox draining; No to direct headless email sending from Obsidian.**
  - **Archiving captured emails into Obsidian is a high-leverage addition.** It removes browser context switching, creates permanent, offline-searchable reference notes, and allows GTD tasks to link directly to local reference material.
  - **Direct headless sending from Obsidian is dangerous and should NOT be built as conceived.** Sending email is an irreversible real-world mutation. Headless automation risks sending confidential vault markers, raw Markdown syntax, internal block IDs (`^1a2b3c`), or private links (`[[secret_project]]`) to external recipients. Furthermore, your existing `gog` authorization for `bryanbugyi34@gmail.com` is strictly read-only (`gmail.readonly`). We recommend a **Draft-First Architecture**: Obsidian creates native Gmail drafts via `bob gmail draft` and opens the web compose interface, or sends via an attended CLI command (`bob gmail send`) guarded by interactive preview and explicit human confirmation.

- **Critical Technical Roadblock: The `FMfcgz...` URL Token Cannot Be Queried Directly via the Gmail API.**
  - Live API testing confirms that the example URL token `FMfcgzQhWTsNRgxMhQNwhZDfgqwXpPsx` is a dynamic, client-side session sync token generated by the modern Gmail web UI. Passing it to Google's REST API (`messages.get` or `threads.get`) immediately fails:
    ```console
    $ gog --account bryanbugyi34@gmail.com gmail get FMfcgzQhWTsNRgxMhQNwhZDfgqwXpPsx
    Google API error (400 invalidArgument): Invalid id value
    ```
  - The token cannot be mathematically or cryptographically decrypted offline (it is an opaque payload encrypted with per-account, server-side keys).
  - **The Solution:** We establish four complementary resolution paths:
    1. *DOM-Assisted Capture:* Bob Mac Capture and browser bookmarklets query the active browser DOM's `[data-legacy-thread-id]` attribute, extracting the canonical 16-hex thread ID (`18cb080b4317f2bc`) at capture time.
    2. *Canonical URL Support:* Support URLs in the format `https://mail.google.com/mail/?authuser=...#all/<hex_id>`.
    3. *Search-Based Heuristic Fallback:* If a bare `FMfcgz...` token is pasted manually without DOM context, `bob gmail` queries recent inbox threads within a narrow time window or queries matching subject tokens if present in the capture line.
    4. *Obsidian Quick Picker:* An Obsidian command (`Ctrl+P` → *Bob: Clip Email from Inbox*) that uses `gog gmail search` to let you pick the message interactively.

- **Preserve Bob's Capture Invariants (Two-Phase Capture):**
  - In Bob, `bob capture` and Bob Mac Capture must remain lightning-fast (<100ms) and offline-resilient. Fetching emails synchronously over the network during live capture breaks the 20-second Mac app timeout and stalls live preview.
  - Like web article clipping (`url_capture_ref_intake_routing`), email clipping must use **Two-Phase Capture**: capture records a durable clip job and immediately inserts a placeholder link; a background worker executes the fetch, writes the note, and rewrites the link. If fetching fails, the raw URL remains preserved as a standard GTD task with a failure badge.

---

## Key Findings & Recommendations

### 1. Vault Storage & Aesthetics
- **Location:** Email notes live in `~/bob/ref/email/YYYY-MM-DD_<sender_slug>_<subject_slug>.md`, integrating directly into Bob's Reference Library (`ref/papers/`, `ref/notes/`, `ref/blogs/`).
- **Frontmatter:** Standardized Dataview-compatible YAML (`type: "[[ref]]"`, `ref_type: email`, `status: read`, `parent: "[[email_ref]]"`, `sender`, `recipients`, `gmail_thread_id`, `gmail_url`, `message_count`).
- **Visual Design:** Notes render using Obsidian Callouts (`> [!email]`) mimicking a modern email client:
  - Header card with sender pill, date badge, and direct `[Open in Gmail ↗]` link.
  - Chronological stacked callouts for multi-message conversation threads (`> [!email|clean]`).
  - Attachment chips linking to `.bob/attachments/email/<thread_id>/` (files >5 MB remain download-on-demand to prevent git vault bloat).
  - Custom CSS snippet: `.obsidian/snippets/bob-email.css`.

### 2. Capture Replacement Syntax
When an email is captured from a task, the raw URL is replaced with a clean wikilink:
```markdown
- [ ] Follow up on contract [[ref/email/2026-11-05_alice_contract|📧 Alice Smith: Q4 Contract Review]] [created:: 2026-11-05]
```

### 3. Safe Email Authoring & Sending
Instead of unsafe headless sending from Obsidian, we recommend a 3-tier model:
- **Tier 1 (Web Compose Deep-Link):** Zero API scopes; opens pre-filled Gmail web compose.
- **Tier 2 (Native Gmail Draft Creation):** `bob gmail draft <path>` converts a markdown draft note into an official Gmail Draft via `gog gmail drafts create` and hands off the web draft URL for final human review and sending.
- **Tier 3 (Attended CLI Send):** `bob gmail send` provides a full terminal diff/preview with an interactive confirmation gate (`y/N`).

### 4. High-Value Spinoff Features
1. **`bob gmail pull` (Inbox Zero Sync):** Drains starred or `#todo`-labeled emails into `~/bob/gmail_inbox.md` as GTD tasks (mirroring `bob gkeep pull`). Checking off the task can optionally archive/un-star the thread in Gmail.
2. **People / CRM Vault Linking:** Auto-links sender email addresses to person notes in the vault (e.g. `[[who/alice|Alice Smith]]`).
3. **Meeting Alignment:** Cross-references calendar event invites with `bob gcal` Event Tasks on today's daily note.

---

## Requirements Adjustments Summary

- **ADJ-1 (URL Ingestion):** Differentiate between web UI tokens (`FMfcgz...`) and API hex IDs; extract `data-legacy-thread-id` via browser DOM where possible, falling back to search heuristics.
- **ADJ-2 (Two-Phase Capture):** Decouple capture UI (<100ms) from network fetching via durable clip jobs.
- **ADJ-3 (Thread Snapshot Semantics):** Email notes represent a captured thread snapshot at capture time, refreshed on demand via `bob gmail sync`.
- **ADJ-4 (Draft-First Authoring):** Replace direct headless email sending with draft generation and web hand-off.
- **ADJ-5 (Reference Library Location):** Place email notes in `ref/email/` under the standard Reference Library structure.
- **ADJ-6 (Attachment Ceiling):** Cap automatic attachment storage at 5 MB to protect git repository performance.

---

## CLI Specification (`bob gmail`)

```console
bob gmail
  Project Google Mail threads into Obsidian vault notes and GTD tasks

SUBCOMMANDS:
  doctor              Diagnose gog installation, account auth, and vault targets
  clip <URL|ID>       Fetch email thread and output replacement Markdown link
  get <THREAD_ID>     Fetch email and print rendered Markdown to stdout
  search <QUERY>      Search Gmail threads via gog and return formatted links
  pull                Drain starred/#todo emails into ~/bob/gmail_inbox.md
  sync [NOTE]         Re-fetch and update an existing email note with new replies
  draft <NOTE_PATH>   Convert a draft note into a Gmail web draft
  send <NOTE_PATH>    Attended CLI send with mandatory confirmation [Interactive]
```

The full research report with detailed architecture diagrams, live API reproduction traces, frontmatter schemas, and phased implementation plans is stored in [`sase/repos/research/202611/bob_gmail_vault_integration__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_37/sase/repos/research/202611/bob_gmail_vault_integration__gem.md).
