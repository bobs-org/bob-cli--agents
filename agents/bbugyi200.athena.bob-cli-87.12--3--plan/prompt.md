%queue(weight=1)
#fork:bob-cli-87.12--2
%model:grok-4.6@high

%macros_enabled:false
# Monitored command finished

**Command:**

```text
/tmp/bob-cli-87.12-mac-corpus-gate.sh
```

**Directory:**

```text
/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12
```

| | |
| --- | --- |
| **Outcome** | COMPLETED — exit 0 |
| **Started** | 2026-10-17T12:07:54.282558+00:00 |
| **Finished** | 2026-10-17T12:23:16.137880Z |
| **Elapsed** | 15m 20s of a 6h 0m 0s budget |
| **Output** | 14 KiB · evidence refs: `file:monitor-diagnostic-manifest:c9rsepw43txv`, `file:monitor-retained-log:c9rsepw43txv` · raw output omitted: `facts_only` · full log: `sase monitor show c9rsepw43txv --all-lines` |

**Why this was monitored:** Run Mac note-snapshot corpus gate after confirmed user-mode tlmgr install of titlesec/enumitem/lastpage

## Continuation checkpoint

- **Ref:** `local:continuation/checkpoints/monitor_start-20ca0191322c0b6e.json`

**Checkpoint (JSON):**

```text
{
  "kind": "monitor_start",
  "payload": {
    "command": "/tmp/bob-cli-87.12-mac-corpus-gate.sh",
    "cwd": "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12",
    "member_agent_name": "bob-cli-87.12--mon",
    "monitor_id": "c9rsepw43txv",
    "next_output": "auto",
    "parent_node_ids": [],
    "project_name": "gh_bobs-org__bob-cli",
    "request_fingerprint": "sha256:7c93e2a7ecc4d21cc47d08054093dc30b6d784dd49cb542d00992fa5c7b10e22",
    "starter_agent": "bob-cli-87.12--2",
    "starter_artifacts_dir": "/home/bryan/.sase/projects/gh_bobs-org__bob-cli/artifacts/ace-run/202610/17/20261017080202"
  },
  "recorded_at_epoch": 1792238875.4707968,
  "schema_version": 1
}
```


## Your next action

Continue bob-cli-87.12 mac-acceptance after the Mac corpus gate monitor.

Assigned bead: bob-cli-87.12 (phase of epic bob-cli-87). Do not close the parent epic. Do not create beads; append PROPOSED FOLLOW-UP notes on bob-cli-87.12. DECISIONS are final: default_text_layer=yes, obsidian_command=yes, decision_record=no (do not edit decisions; record a PROPOSED FOLLOW-UP suggesting annotated-pdfs-render-on-xelatex). Never copy vault content into the bob-cli repo.

Already done:
- Mac deploy of df4e120 at /Users/bbugyi/projects/github/bobs-org/bob-cli; bob plugins sync up to date.
- pdfkit_probe.swift at mac:/tmp/pdfkit_probe.swift (usage: swift pdfkit_probe.swift vocab.txt a.pdf [b.pdf ...]).
- TeX user tree inited at ~/Library/texmf.
- Gate custom-0d798ba5 answered Install. tlmgr --usermode did install titlesec, enumitem, lastpage; the gate script then failed on `printf --`. Confirmed after the gate: kpsewhich finds all three .sty under ~/Library/texmf; bob ref doctor latex_packages: ok (30 checked). Do not reinstall.
- Toolchain on Mac: pandoc 3.11, XeTeX TeX Live 2026 (XeTeX 3.141592653-2.6-0.999998), bob 0.1.0 from ~/.cargo/bin, HEAD df4e120.
- SSH: `ssh -o ForwardX11=no mac 'bash -lc "..."'` (or export PATH to include /Users/bbugyi/.cargo/bin:/opt/homebrew/bin:/Library/TeX/texbin). Use ServerAliveInterval for long sessions.

Corpus gate (this monitor):
- Command wrapper: /tmp/bob-cli-87.12-mac-corpus-gate.sh
- Output PDFs + summary: mac:/tmp/bob-note-snap-out (summary.md at the top lists render/dry-run counts, failures, missing glyphs, Type 3, overfull, vault git unchanged).
- Kept workdirs + projected.md: mac:/tmp/bob-note-snap-gate/bob-*-* (BOB_HIGHLIGHTS_KEEP_WORKDIR=1, TMPDIR=/tmp/bob-note-snap-gate). Each render log mac:/tmp/bob-note-snap-out/logs/render-NNNN.log should contain a `workdir:` line pairing that PDF to its projected.md.

1. Read the monitor result and mac:/tmp/bob-note-snap-out/summary.md. Pass criteria match athena: 100% render, 0 missing glyphs, 0 Type 3, 0 overfull, vault git unchanged. If the gate failed, diagnose (BasicTeX, missing packages, vault dirty, SSH drop); do not install TeX packages silently — re-gate if another tlmgr install is needed. Record numbers on the bead. If it failed for a reason that reproduces on a clean tree, PROPOSED FOLLOW-UP and still close only after the rest of this phase that can still complete; a corpus-gate fail is this phase's job to fix or explain.

2. PDFKit probe over every corpus PDF. Vocab = corresponding projected.md (the kept workdir for that render, not the live vault note). Require 0 unexplained non-source words. Pair via the `workdir:` line in each render log. Also probe one research-report PDF because markdown-text-layer landed (find an in-vault research-report PDF under ~/bob; do not copy vault bytes into the repo). Write probe output to mac:/tmp/bob-note-snap-out/pdfkit-probe.txt.

3. Real Highlights round trip with Bryan: `bob ref create sase_blog` (intake, not -o), then `bob ref scan`. Use /sase_questions to ask Bryan to open it in Highlights; highlight a task line, a prose quote, and an image; add one #task comment; run bob ref sync or wait for cron. Verify quotes byte-clean vs PDF text, follow-up task in sase_blog.md, source_note [[sase_blog]], chips in quotes acceptable (try accsupp ActualText={} on chips only if they pollute quotes). If highlights:// links would open refs, record a PROPOSED FOLLOW-UP.

4. Record a Verified on athena and the Mac section in docs/highlights-create.md: dates, pandoc and TeX versions, gate numbers, probe result, round-trip PASS. No vault text. Athena numbers already live under Verified on athena (2026-10-16: 101 renders, 5054 dry-runs, 0 failures/glyphs/Type3/overfull, vault unchanged).

5. decision_record=no: PROPOSED FOLLOW-UP for the decisions-web strand annotated-pdfs-render-on-xelatex; do not write the memory note.

6. Before close: sase bead epic-symbols bob-cli-87.12 and resolve leftovers. Close only bob-cli-87.12 with a note of what you verified.
%macros_enabled:true