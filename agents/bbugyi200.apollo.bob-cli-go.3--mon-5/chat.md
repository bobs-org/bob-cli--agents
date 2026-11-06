# Chat History - ace-run (bob-cli-go.3--mon-5)

- **TIMESTAMP:** 2026-11-03 19:50:46 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-go.3--mon-5

## Prompt

sase monitor start --command 'cargo run --quiet -- task split --help && just docs-check' --reason 'Verify task split CLI help and generated docs checks'

## Response

sase tool run fb4676e4ea51d23c2bcca2957fc68523
Split selected authored bullets from a task into new tasks. The parent keeps an in-place task link to each new task, and the selected bullets' children move with them. A live run uses the task maintenance lock, guarded writes, a scoped commit, and vault sync; --dry-run prints the same plan without changing the vault.

Usage: bob task split [OPTIONS] <TASK|NOTE>

Arguments:
  <TASK|NOTE>
          Task locator, or note path when --section is given

Options:
  -d, --dry-run
          Plan and print only; do not lock, sync, or write

  -f, --format <FORMAT>
          Output format: human or json
          
          [default: human]
          [possible values: human, json]

  -h, --help
          Show help

  -m, --match <TEXT>
          Select a unique splittable bullet containing this text; repeatable

  -n, --nth <N>
          Select the Nth candidate; repeatable and 1-based

  -o, --offline
          Skip both sync cycles; commit locally

  -r, --retry-timeout <SECONDS>
          Lock wait and re-plan budget
          
          [default: 60]

  -s, --section <TITLE>
          Select section bullets in this note; created Tasks intake receives the new tasks

Examples:
  bob task split --dry-run db:upgrade -n 1
                                 Preview the first splittable note
  bob task split db:upgrade -m 'rollback runbook'
                                 Split the unique matching note
  bob task split dev -s 'Future Work'
                                 Promote every bullet in a note section
  bob task split -f json db:upgrade
                                 List numbered candidates as JSON

A task locator is note:block-id or [[note#^block-id]].

✅  DOCS CHECK
────────────────────────────────────────────────
uv run --project tools/docs bob-docs check
docs-check: assemble and validate source context

docs-check: lint
bob-docs lint: ok
docs-check: passed (lint)

docs-check: generated drift
bob-docs: error: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/memory/glossary/task-merge.md: memory strand has no front matter
error: Recipe `docs-check` failed on line 269 with exit code 2
failed  exit=2  duration=206813ms

