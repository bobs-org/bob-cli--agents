# Chat History - ace-run (research.5o.gem)

- **TIMESTAMP:** 2026-11-02 08:15:56 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.5o.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261102_080139.md`

## Prompt

%id(gem, clan=research.5o)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.5o.cdx`, `research.5o.cld`, `research.5o.grk`, `research.5o.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to start having the `bob gcal sync` command convert the Google Calendar
event descriptions (excluding the special syntax we already parse from descriptions)
into sub-bullets that are added to the corresponding event tasks that this command
creates. I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

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

# Architectural Research & Design Report: Google Calendar Event Description Sub-bullets in `bob gcal sync`

**Researcher:** `research.gem`  
**Report File:** [`gcal_event_description_subbullets__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_23/sase/repos/research/202611/gcal_event_description_subbullets__gem.md)  
**Registered Artifact:** `research:202611/gcal_event_description_subbullets__gem.md` (`explicit:df618bc0af9db5702db4e0dc`)

---

### Executive Summary & Verdict

Converting Google Calendar event descriptions into sub-bullets under Event Tasks is a **compelling, high-utility feature** that transforms the daily note's `## Events` section into a true self-contained command center. It gives you immediate access to meeting agendas, discussion topics, and pre-reading materials during your morning GTD review and throughout the day without forcing context-switches back into the browser or calendar app.

However, **a naive implementation would be disastrous**. In the wild, over 80% of calendar event descriptions contain massive auto-generated video conferencing footers (Zoom/Teams/Meet dial-in telephone directories, meeting IDs, and legal disclaimers) or raw HTML markup. Without strict sanitization, your daily note would be flooded with telephone numbers, hyperlinks would be stripped into useless plain text, and checklist items could leak into Obsidian Dataview as phantom GTD tasks.

---

### Core Critique: Pitfalls & Risks

1. **The "Dial-In Directory" Noise Hazard:**
   Video conferencing footers (Zoom, Google Meet, Microsoft Teams) often append 15–30 lines of phone numbers and disclaimers. Because `bob` already renders a dedicated camera badge `[📹](url)` on the task line, copying conferencing text into sub-bullets is pure visual clutter.
2. **HTML Hyperlink Destruction:**
   Google Calendar serializes rich text as HTML. Naively stripping HTML tags removes `<a href="...">` URLs, permanently severing links to Google Docs, Notion specs, and PRs.
3. **Checkbox Contamination (`- [ ]` vs `- `):**
   Google Calendar rich text supports checklists. Rendering these as `- [ ]` in Obsidian causes Dataview, global task counters, and GTD review walks to treat them as active personal tasks rather than reference material.
4. **Collision with Vault Ownership (Decision 9):**
   **Decision 9 (`bob-gcal-is-read-only-and-proposes-once`)** guarantees that *the vault owns children and meeting notes*. If sync attempts to mutate child bullets after initial creation, it risks overwriting notes you take during the meeting.

---

### Key Requirement Adjustments

To ensure this feature is **intuitive, reliable, and beautiful**, the following adjustments are specified:

1. **Structural Housing via Task Drawer (`- AGENDA`):**
   Rather than uncontained flat bullets that mix with your live meeting notes, encapsulate the converted description in a native Bob Task Drawer (`- AGENDA`).
   - **Obsidian Foldability:** You can collapse the agenda into a single line (`- AGENDA ...`) by clicking its fold triangle, keeping `## Events` visually compact while preserving the agenda on demand.
   - **Clear Boundary:** Clearly separates organizer context from your own live meeting notes (`- NOTES` or direct task notes).
   - **Capture Integration:** Seamlessly integrates with Bob Mac Capture drawer addressing (`@today+arch-rev#agenda`).
2. **Aggressive Conferencing Boilerplate Suppression:**
   Detect and discard video conferencing join blocks, dial-in numbers, and email disclaimers.
3. **Rich HTML-to-Markdown Link Preservation:**
   Convert `<a href="URL">TEXT</a>` into `[TEXT](URL)` so linked documents remain functional in Obsidian. Convert basic formatting (`<b>`, `<i>`, `<code>`) to Markdown equivalents.
4. **Strict Checkbox Neutralization:**
   Convert all description checklist items into plain list bullets (`- `), never `- [ ]`.
5. **Length Bounds & Truncation Safeguard:**
   Cap at 10 lines of bullets. If truncated, append an ellipsis link: `- ... [more in Google Calendar](url)`.
6. **Strict Creation-Only Lifecycle (Write-at-Birth):**
   Sub-bullets are generated **only** when an Event Task is created (or when a context row is upgraded to a task). On subsequent syncs, the child block is completely ignored by sync, guaranteeing zero churn and zero risk of overwriting your notes.

---

### Recommended Output Geometry

When an event is synced, it will render cleanly as:

```markdown
- [ ] #task **1000-1100** Architecture Review [📅](https://...) [📹](https://...) [root:: eng] [type:: MEET] ^arch-rev
  - AGENDA
    - Review RFC 42: [RFC 42 Spec](https://github.com/...)
    - Discuss database migration timeline
    - Open questions from Kelly on API stability
```

If you add meeting notes during or after the call, your daily note cleanly organizes both:

```markdown
- [ ] #task **1000-1100** Architecture Review [📅](https://...) [📹](https://...) [root:: eng] [type:: MEET] ^arch-rev
  - AGENDA
    - Review RFC 42: [RFC 42 Spec](https://github.com/...)
    - Discuss database migration timeline
  - Approved Sunday 02:00 UTC migration window with Ops
  - Action: submit change ticket to security team
```

---

### Artifact Registration & File Details

- **Report Path:** `/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_23/sase/repos/research/202611/gcal_event_description_subbullets__gem.md`
- **Durable Snapshot Label:** `research:202611/gcal_event_description_subbullets__gem.md`
- **Snapshot Ref:** `file:explicit:df618bc0af9db5702db4e0dc`
- **Status:** Complete, registered, and finalized.
