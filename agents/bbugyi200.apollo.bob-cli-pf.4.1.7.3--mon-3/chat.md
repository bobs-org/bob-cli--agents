# Chat History - ace-run (bob-cli-pf.4.1.7.3--mon-3)

- **TIMESTAMP:** 2026-11-23 07:31:10 EST
- **MODEL:** codex/gpt-6-astra
- **AGENT:** bob-cli-pf.4.1.7.3--mon-3

## Prompt

sase monitor start --command 'python3 .git/property-editor-acceptance-run.py' --reason 'Verify property editor input focus and canonical-record routing with complete write acceptance'

## Response

sase tool run ff77158b573d00911b632eb83665fefc
Validating plugin build and manifests
validate exit: 0
Running the complete plugin suite after browse and new-stage focus fixes
npm test exit: 1; log: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.git/property-editor-acceptance-results/npm-test.log
Checking the two known timing suites in isolation
isolated timing exit: 0
Fresh acceptance directory on athena: /tmp/bob-property-editor-writes.2VhMoL
Building the clean CLI and running real Obsidian acceptance
{
  "remote": "/tmp/bob-property-editor-writes.2VhMoL",
  "npmTestExit": 1,
  "isolatedTimingExit": 0,
  "validateExit": 0,
  "acceptanceExit": 1,
  "copyExit": 0,
  "output": "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/.git/property-editor-acceptance-results",
  "pass": false,
  "error": "Timed out waiting for Tab accepts known tags type: {\"open\":true,\"readSettled\":true,\"focusedRow\":\"\",\"heading\":\"PROJECT \u00b7 PROPERTIES\",\"rows\":[{\"key\":\"parent\",\"id\":\"parent::4\",\"line\":4,\"action\":\"edit\",\"disabled\":false,\"selected\":false,\"text\":\"\u2261parent[[projects]]\",\"valueText\":\"[[projects]]\",\"diagnostic\":\"\"},{\"key\":\"launch_window\",\"id\":\"launch_window::5\",\"line\":5,\"action\":\"edit\",\"disabled\":false,\"selected\":false,\"text\":\"\u2261launch_windowready\",\"valueText\":\"ready\",\"diagnostic\":\"\"},{\"key\":\"keep_exact\",\"id\":\"keep_exact::6\",\"line\":6,\"action\":\"edit\",\"disabled\":false,\"selected\":false,\"text\":\"\u2261keep_exactkeep : and # exactly\",\"valueText\":\"keep : and # exactly\",\"diagnostic\":\"\"},{\"key\":\"locked_toggle\",\"id\":\"locked_toggle::9\",\"line\":9,\"action\":\"toggle\",\"disabled\":false,\"selected\":true,\"text\":\"\u2611locked_toggle\u2717\",\"valueText\":\"\u2717\",\"diagnostic\":\"\"},{\"key\":\"added_field\",\"id\":\"added_field::10\",\"line\":10,\"action\":\"edit\",\"disabled\":false,\"selected\":false,\"text\":\"\u2261added_fieldfrom-editor\",\"valueText\":\"from-editor\",\"diagnostic\":\"\"},{\"key\":\"type\",\"id\":\"type::3\",\"line\":3,\"action\":\"locked\",\"disabled\":true,\"selected\":false,\"text\":\"\u2261type[[project]]\",\"valueText\":\"[[project]]\",\"diagnostic\":\"\"},{\"key\":\"project_digest\",\"id\":\"project_digest::7\",\"line\":7,\"action\":\"locked\",\"disabled\":true,\"selected\":false,\"text\":\"\u2261project_digestsha256:0123456789abcdef\",\"valueText\":\"sha256:0123456789abcdef\",\"diagnostic\":\"\"},{\"key\":\"review_enabled\",\"id\":\"review_enabled::8\",\"line\":8,\"action\":\"locked\",\"disabled\":true,\"selected\":false,\"text\":\"\u2611review_enabled\u2717\",\"valueText\":\"\u2717\",\"diagnostic\":\"\"}],\"properties\":[{\"key\":\"type\",\"line\":3,\"kind\":\"text\",\"role\":\"identity\",\"duplicate\":false,\"diagnostic\":\"\"},{\"key\":\"parent\",\"line\":4,\"kind\":\"text\",\"role\":\"loose\",\"duplicate\":false,\"diagnostic\":\"\"},{\"key\":\"launch_window\",\"line\":5,\"kind\":\"text\",\"role\":\"loose\",\"duplicate\":false,\"diagnostic\":\"\"},{\"key\":\"",
  "assertionCounts": {
    "pass": 30
  },
  "bob": {
    "path": "/tmp/bob-property-editor-writes.2VhMoL/bob-cli/target/debug/bob",
    "sha256": "fc40bf67510adf4659bec1926c6dff7f0db11f9a1d125c79031c2328e5d6f371",
    "version": "bob 0.6.0",
    "sourceSha": "de66b399e4d9a9837989687ec172217b32d4238f"
  },
  "failureDiagnostics": {
    "pluginLoaded": true,
    "entrypointsActive": true,
    "layoutReady": true,
    "activePath": "projects/project-note.md",
    "documentUrl": "app://obsidian.md/index.html",
    "documentFocused": true,
    "activeWindowMatches": true,
    "activeDocumentUrl": "app://obsidian.md/index.html",
    "documentEditors": 1,
    "documentModals": 1,
    "modal": {
      "filePath": "projects/project-note.md",
      "closed": false,
      "pendingApply": false,
      "readSeq": 1,
      "status": {
        "kind": "ready",
        "text": "Preview ready \u00b7 Enter saves"
      },
      "refusal": null,
      "reportPath": "projects/project-note.md",
      "stageKind": "text",
      "connected": true,
      "ownerDocumentMatches": true,
      "ownerDocumentUrl": "app://obsidian.md/index.html",
      "ownerDocumentEditors": 1,
      "root": "#document",
      "rootHost": null,
      "contentHtml": "<div class=\"modal-content\"><div class=\"bob-property-editor\" role=\"dialog\" tabindex=\"-1\" aria-label=\"Edit properties \u00b7 projects/project-note.md\"><div class=\"bob-property-editor-header\"><span class=\"bob-property-editor-tile\">\u25a4</span><div class=\"bob-property-editor-titles\"><h2 class=\"bob-property-editor-heading\">PROJECT \u00b7 PROPERTIES</h2><div class=\"bob-property-editor-title\">Project</div><div class=\"bob-property-editor-sub\">projects/project-note.md \u00b7 8 properties</div></div></div><div class=\"bob-property-editor-list\" role=\"listbox\" aria-label=\"Properties\"><div class=\"bob-property-editor-group\" data-property-group=\"loose\"><div class=\"bob-property-editor-group-title\">Loose</div><button class=\"bob-property-row\" type=\"button\" data-property-key=\"parent\" data-property-row=\"parent::4\" role=\"option\" aria-selected=\"false\" data-property-action=\"edit\"><span class=\"bob-property-row-icon\" aria-hidden=\"true\">\u2261</span><span class=\"bob-property-row-key\">parent</span><span class=\"bob-property-row-value\">[[projects]]</span></button><button class=\"bob-property-row\" type=\"button\" data-property-key=\"launch_window\" data-property-row=\"launch_window::5\" role=\"option\" aria-selected=\"false\" data-property-action=\"edit\"><span class=\"bob-property-row-icon\" aria-hidden=\"true\">\u2261</span><span class=\"bob-property-row-key\">launch_window</span><span class=\"bob-property-row-value\">ready</span></button><button class=\"bob-property-row\" type=\"button\" data-property-key=\"keep_exact\" data-property-row=\"keep_exact::6\" role=\"option\" aria-selected=\"false\" data-property-action=\"edit\"><span class=\"bob-property-row-icon\" aria-hidden=\"true\">\u2261</span><span class=\"bob-property-row-key\">keep_exact</span><span class=\"bob-property-row-value\">keep : and # exactly</span></button><button class=\"bob-property-row\" type=\"button\" data-property-key=\"locked_toggle\" data-property-row=\"locked_toggle::9\" role=\"option\" aria-selected=\"true\" aria-current=\"true\" data-property-action=\"toggle\"><span class=\"bob-property-row-icon\" aria-hidden=\"true\">\u2611</span><span class=\"bob-property-row-key\">locked_toggle</span><span class=\"bob-property-row-value\">\u2717</span></button><button class=\"bob-property-row\" type=\"button\" data-property-key=\"added_field\" data-property-row=\"added_field::10\" role=\"option\" aria-selected=\"false\" data-property-action=\"edit\"><span class=\"bob-property-row-icon\" aria-hidden=\"true\">\u2261</span><span class=\"bob-property-row-key\">added_field</span><span class=\"bob-property-row-value\">from-editor</span></button></div><div class=\"bob-property-editor-group\" data-property-group=\"identity\"><div class=\"bob-property-editor-group-title\">Identity</div><button class=\"bob-property-row\" type=\"button\" data-property-key=\"type\" data-property-row=\"type::3\" role=\"option\" aria-selected=\"false\" data-property-action=\"locked\" aria-disabled=\"true\"><span class=\"bob-property-row-icon\" aria-hidden=\"true\">\u2261</span><span class=\"bob-property-row-key\">type</span><span class=\"bob-property-row-value\">[[project]]</span></button></div><div class=\"bob-property-editor-group\" data-property-group=\"managed\"><div class=\"bob-property-editor-group-title\">Bob-managed</div><button class=\"bob-property-row\" type=\"button\" data-property-key=\"project_digest\" data-property-row=\"project_digest::7\" role=\"option\" aria-selected=\"false\" data-property-action=\"locked\" aria-disabled=\"true\"><span class=\"bob-property-row-icon\" aria-hidden=\"true\">\u2261</span><span class=\"bob-property-row-key\">project_digest</span><span class=\"bob-property-row-value\">sha256:0123456789abcdef</span></button><button class=\"bob-property-row\" type=\"button\" data-property-key=\"review_enabled\" data-property-row=\"review_enabled::8\" role=\"option\" aria-selected=\"false\" data-property-action=\"locked\" aria-disabled=\"true\"><span class=\"bob-property-row-icon\" aria-hidden=\"true\">\u2611</span><span class=\"bob-property-row-key\">review_enabled</span><span class=\"bob-property-row-value\">\u2717</span></button></div></div><section class=\"bob-property-editor-stage\" data-property-stage=\"1\" aria-label=\"Edit tags\"><div class=\"bob-property-editor-stage-title\">tags \u00b7 Text</div><label class=\"bob-property-editor-stage-label\" for=\"bob-property-editor-stage-input-1\">New text value</label><textarea class=\"bob-property-editor-stage-input is-text\" rows=\"3\" id=\"bob-property-editor-stage-input-1\" data-property-stage-input=\"property-stage-1\" data-property-stage-id=\"1\" data-property-stage-kind=\"text\" aria-label=\"tags text\" autocomplete=\"on\"></textarea><div class=\"bob-property-editor-stage-prose\" data-property-stage-band=\"1\"></div><div class=\"bob-property-editor-stage-suggestions\" role=\"listbox\" aria-label=\"Existing tags values\"><button class=\"bob-property-editor-stage-suggestion\" type=\"button\" role=\"option\" data-property-stage-action=\"pick-suggestion\" data-property-stage-index=\"0\" aria-label=\"home\">home \u00b7 1</button></div><div class=\"bob-property-editor-stage-preview\" role=\"status\" aria-live=\"polite\">Preview \u00b7 tags = \"\" \u00b7 Enter saves</div><div class=\"bob-property-editor-stage-actions\" role=\"group\" aria-label=\"Property value actions\"><button class=\"bob-property-editor-stage-save\" type=\"button\" data-property-stage-action=\"save\">Save</button><button class=\"bob-property-editor-stage-cancel\" type=\"button\" data-property-stage-action=\"cancel\">Cancel</button></div></section><div class=\"bob-property-editor-status\" role=\"status\" aria-live=\"polite\">Preview ready \u00b7 Enter saves</div><div class=\"bob-property-editor-hints\">j/k move \u00b7 o/O add \u00b7 Mod+; end \u00b7 Enter/l open \u00b7 Ctrl+D delete \u00b7 u undo \u00b7 y YAML \u00b7 Esc close</div></div></div>"
    },
    "lifecycle": [
      {
        "method": "open",
        "path": "projects/project-note.md",
        "closed": false,
        "connected": false,
        "stack": "Error\n    at proto.<computed> [as open] (<anonymous>:20:23)\n    at openPropertyEditor (plugin:bob-ledger-tools:167966:15)\n    at BobLedgerToolsPlugin.openPropertyEditor (plugin:bob-ledger-tools:170321:15)\n    at <anonymous>:5:33\n    at <anonymous>:13:5"
      },
      {
        "method": "onOpen",
        "path": "projects/project-note.md",
        "closed": false,
        "connected": true,
        "stack": "Error\n    at proto.<computed> (<anonymous>:20:23)\n    at PropertyEditorModal.open (app://obsidian.md/app.js:245:25721)\n    at proto.<computed> [as open] (<anonymous>:23:29)\n    at openPropertyEditor (plugin:bob-ledger-tools:167966:15)\n    at BobLedgerToolsPlugin.openPropertyEditor (plugin:bob-ledger-tools:170321:15)\n    at <anonymous>:5:33\n    at <anonymous>:13:5"
      },
      {
        "method": "close",
        "path": "projects/project-note.md",
        "closed": false,
        "connected": true,
        "stack": "Error\n    at proto.<computed> [as close] (<anonymous>:20:23)\n    at modal.close (plugin:bob-ledger-tools:170348:16)\n    at PropertyEditorModal.propertyEditorPerform (plugin:bob-ledger-tools:167540:18)\n    at PropertyEditorModal.propertyEditorPerform (plugin:bob-ledger-tools:169867:43)\n    at PropertyEditorModal.propertyEditorOnKeyDown (plugin:bob-ledger-tools:167472:15)\n    at PropertyEditorModal.propertyEditorOnKeyDown (plugin:bob-ledger-tools:169074:42)\n    at PropertyEditorModal.propertyEditorOnKeyDown (plugin:bob-ledger-tools:169917:39)\n    at HTMLDivElement.<anonymous> (plugin:bob-ledger-tools:167294:60)"
      },
      {
        "method": "onClose",
        "path": "projects/project-note.md",
        "closed": false,
        "connected": false,
        "stack": "Error\n    at proto.<computed> (<anonymous>:20:23)\n    at r (app://obsidian.md/app.js:245:26566)\n    at PropertyEditorModal.close (app://obsidian.md/app.js:245:26647)\n    at proto.<computed> [as close] (<anonymous>:23:29)\n    at modal.close (plugin:bob-ledger-tools:170348:16)\n    at PropertyEditorModal.propertyEditorPerform (plugin:bob-ledger-tools:167540:18)\n    at PropertyEditorModal.propertyEditorPerform (plugin:bob-ledger-tools:169867:43)\n    at PropertyEditorModal.propertyEditorOnKeyDown (plugin:bob-ledger-tools:167472:15)\n    at PropertyEditorModal.propertyEditorOnKeyDown (plugin:bob-ledger-tools:169074:42)\n    at PropertyEditorModal.propertyEditorOnKeyDown (plugin:bob-ledger-tools:169917:39)"
      },
      {
        "method": "open",
        "path": "projects/project-note.md",
        "closed": false,
        "connected": false,
        "stack": "Error\n    at proto.<computed> [as open] (<anonymous>:20:23)\n    at openPropertyEditor (plugin:bob-ledger-tools:167966:15)\n    at BobLedgerToolsPlugin.openPropertyEditor (plugin:bob-ledger-tools:170321:15)\n    at BobLedgerToolsPlugin.propertyEditorYamlDoneAttempt (plugin:bob-ledger-tools:170614:31)\n    at process.processTicksAndRejections (node:internal/process/task_queues:104:5)\n    at async BobLedgerToolsPlugin.albumYamlDone (plugin:bob-ledger-tools:69647:14)"
      },
      {
        "method": "onOpen",
        "path": "projects/project-note.md",
        "closed": false,
        "connected": true,
        "stack": "Error\n    at proto.<computed> (<anonymous>:20:23)\n    at PropertyEditorModal.open (app://obsidian.md/app.js:245:25721)\n    at proto.<computed> [as open] (<anonymous>:23:29)\n    at openPropertyEditor (plugin:bob-ledger-tools:167966:15)\n    at BobLedgerToolsPlugin.openPropertyEditor (plugin:bob-ledger-tools:170321:15)\n    at BobLedgerToolsPlugin.propertyEditorYamlDoneAttempt (plugin:bob-ledger-tools:170614:31)\n    at process.processTicksAndRejections (node:internal/process/task_queues:104:5)\n    at async BobLedgerToolsPlugin.albumYamlDone (plugin:bob-ledger-tools:69647:14)"
      },
      {
        "method": "close",
        "path": "projects/project-note.md",
        "closed": false,
        "connected": true,
        "stack": "Error\n    at proto.<computed> [as close] (<anonymous>:20:23)\n    at modal.close (plugin:bob-ledger-tools:170348:16)\n    at PropertyEditorModal.propertyEditorPerform (plugin:bob-ledger-tools:167540:18)\n    at PropertyEditorModal.propertyEditorPerform (plugin:bob-ledger-tools:169867:43)\n    at PropertyEditorModal.propertyEditorOnKeyDown (plugin:bob-ledger-tools:167472:15)\n    at PropertyEditorModal.propertyEditorOnKeyDown (plugin:bob-ledger-tools:169074:42)\n    at PropertyEditorModal.propertyEditorOnKeyDown (plugin:bob-ledger-tools:169917:39)\n    at HTMLDivElement.<anonymous> (plugin:bob-ledger-tools:167294:60)"
      },
      {
        "method": "onClose",
        "path": "projects/project-note.md",
        "closed": false,
        "connected": false,
        "stack": "Error\n    at proto.<computed> (<anonymous>:20:23)\n    at r (app://obsidian.md/app.js:245:26566)\n    at PropertyEditorModal.close (app://obsidian.md/app.js:245:26647)\n    at proto.<computed> [as close] (<anonymous>:23:29)\n    at modal.close (plugin:bob-ledger-tools:170348:16)\n    at PropertyEditorModal.propertyEditorPerform (plugin:bob-ledger-tools:167540:18)\n    at PropertyEditorModal.propertyEditorPerform (plugin:bob-ledger-tools:169867:43)\n    at PropertyEditorModal.propertyEditorOnKeyDown (plugin:bob-ledger-tools:167472:15)\n    at PropertyEditorModal.propertyEditorOnKeyDown (plugin:bob-ledger-tools:169074:42)\n    at PropertyEditorModal.propertyEditorOnKeyDown (plugin:bob-ledger-tools:169917:39)"
      },
      {
        "method": "open",
        "path": "projects/project-note.md",
        "closed": false,
        "connected": false,
        "stack": "Error\n    at proto.<computed> [as open] (<anonymous>:20:23)\n    at openPropertyEditor (plugin:bob-ledger-tools:167966:15)\n    at BobLedgerToolsPlugin.openPropertyEditor (plugin:bob-ledger-tools:170321:15)\n    at BobLedgerToolsPlugin.propertyEditorYamlDoneAttempt (plugin:bob-ledger-tools:170614:31)\n    at process.processTicksAndRejections (node:internal/process/task_queues:104:5)\n    at async BobLedgerToolsPlugin.albumYamlDone (plugin:bob-ledger-tools:69647:14)"
      },
      {
        "method": "onOpen",
        "path": "projects/project-note.md",
        "closed": false,
        "connected": true,
        "stack": "Error\n    at proto.<computed> (<anonymous>:20:23)\n    at PropertyEditorModal.open (app://obsidian.md/app.js:245:25721)\n    at proto.<computed> [as open] (<anonymous>:23:29)\n    at openPropertyEditor (plugin:bob-ledger-tools:167966:15)\n    at BobLedgerToolsPlugin.openPropertyEditor (plugin:bob-ledger-tools:170321:15)\n    at BobLedgerToolsPlugin.propertyEditorYamlDoneAttempt (plugin:bob-ledger-tools:170614:31)\n    at process.processTicksAndRejections (node:internal/process/task_queues:104:5)\n    at async BobLedgerToolsPlugin.albumYamlDone (plugin:bob-ledger-tools:69647:14)"
      },
      {
        "method": "close",
        "path": "projects/project-note.md",
        "closed": false,
        "connected": true,
        "stack": "Error\n    at proto.<computed> [as close] (<anonymous>:20:23)\n    at modal.close (plugin:bob-ledger-tools:170348:16)\n    at PropertyEditorModal.propertyEditorPerform (plugin:bob-ledger-tools:167540:18)\n    at PropertyEditorModal.propertyEditorPerform (plugin:bob-ledger-tools:169867:43)\n    at PropertyEditorModal.propertyEditorOnKeyDown (plugin:bob-ledger-tools:167472:15)\n    at PropertyEditorModal.propertyEditorOnKeyDown (plugin:bob-ledger-tools:169074:42)\n    at PropertyEditorModal.propertyEditorOnKeyDown (plugin:bob-ledger-tools:169917:39)\n    at HTMLDivElement.<anonymous> (plugin:bob-ledger-tools:167294:60)"
      },
      {
        "method": "onClose",
        "path": "projects/project-note.md",
        "closed": false,
        "connected": false,
        "stack": "Error\n    at proto.<computed> (<anonymous>:20:23)\n    at r (app://obsidian.md/app.js:245:26566)\n    at PropertyEditorModal.close (app://obsidian.md/app.js:245:26647)\n    at proto.<computed> [as close] (<anonymous>:23:29)\n    at modal.close (plugin:bob-ledger-tools:170348:16)\n    at PropertyEditorModal.propertyEditorPerform (plugin:bob-ledger-tools:167540:18)\n    at PropertyEditorModal.propertyEditorPerform (plugin:bob-ledger-tools:169867:43)\n    at PropertyEditorModal.propertyEditorOnKeyDown (plugin:bob-ledger-tools:167472:15)\n    at PropertyEditorModal.propertyEditorOnKeyDown (plugin:bob-ledger-tools:169074:42)\n    at PropertyEditorModal.propertyEditorOnKeyDown (plugin:bob-ledger-tools:169917:39)"
      },
      {
        "method": "open",
        "path": "projects/project-note.md",
        "closed": false,
        "connected": false,
        "stack": "Error\n    at proto.<computed> [as open] (<anonymous>:20:23)\n    at openPropertyEditor (plugin:bob-ledger-tools:167966:15)\n    at BobLedgerToolsPlugin.openPropertyEditor (plugin:bob-ledger-tools:170321:15)\n    at BobLedgerToolsPlugin.propertyEditorYamlDoneAttempt (plugin:bob-ledger-tools:170614:31)\n    at async BobLedgerToolsPlugin.albumYamlDone (plugin:bob-ledger-tools:69647:14)"
      },
      {
        "method": "onOpen",
        "path": "projects/project-note.md",
        "closed": false,
        "connected": true,
        "stack": "Error\n    at proto.<computed> (<anonymous>:20:23)\n    at PropertyEditorModal.open (app://obsidian.md/app.js:245:25721)\n    at proto.<computed> [as open] (<anonymous>:23:29)\n    at openPropertyEditor (plugin:bob-ledger-tools:167966:15)\n    at BobLedgerToolsPlugin.openPropertyEditor (plugin:bob-ledger-tools:170321:15)\n    at BobLedgerToolsPlugin.propertyEditorYamlDoneAttempt (plugin:bob-ledger-tools:170614:31)\n    at async BobLedgerToolsPlugin.albumYamlDone (plugin:bob-ledger-tools:69647:14)"
      }
    ],
    "lastOpen": {
      "filePath": "projects/project-note.md",
      "ok": true,
      "reason": null,
      "message": null,
      "connected": true,
      "documentEditors": 1
    }
  }
}
Last build/acceptance log lines:
Note: switching to 'de66b399e4d9a9837989687ec172217b32d4238f'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.95s
FAIL Property Editor e2e ({"pass":30})
Report: /tmp/bob-property-editor-writes.2VhMoL/results/property-editor-report.json
Screenshots: /tmp/bob-property-editor-writes.2VhMoL/results/shots
- Timed out waiting for Tab accepts known tags type: {"open":true,"readSettled":true,"focusedRow":"","heading":"PROJECT · PROPERTIES","rows":[{"key":"parent","id":"parent::4","line":4,"action":"edit","disabled":false,"selected":false,"text":"≡parent[[projects]]","valueText":"[[projects]]","diagnostic":""},{"key":"launch_window","id":"launch_window::5","line":5,"action":"edit","disabled":false,"selected":false,"text":"≡launch_windowready","valueText":"ready","diagnostic":""},{"key":"keep_exact","id":"keep_exact::6","line":6,"action":"edit","disabled":false,"selected":false,"text":"≡keep_exactkeep : and # exactly","valueText":"keep : and # exactly","diagnostic":""},{"key":"locked_toggle","id":"locked_toggle::9","line":9,"action":"toggle","disabled":false,"selected":true,"text":"☑locked_toggle✗","valueText":"✗","diagnostic":""},{"key":"added_field","id":"added_field::10","line":10,"action":"edit","disabled":false,"selected":false,"text":"≡added_fieldfrom-editor","valueText":"from-editor","diagnostic":""},{"key":"type","id":"type::3","line":3,"action":"locked","disabled":true,"selected":false,"text":"≡type[[project]]","valueText":"[[project]]","diagnostic":""},{"key":"project_digest","id":"project_digest::7","line":7,"action":"locked","disabled":true,"selected":false,"text":"≡project_digestsha256:0123456789abcdef","valueText":"sha256:0123456789abcdef","diagnostic":""},{"key":"review_enabled","id":"review_enabled::8","line":8,"action":"locked","disabled":true,"selected":false,"text":"☑review_enabled✗","valueText":"✗","diagnostic":""}],"properties":[{"key":"type","line":3,"kind":"text","role":"identity","duplicate":false,"diagnostic":""},{"key":"parent","line":4,"kind":"text","role":"loose","duplicate":false,"diagnostic":""},{"key":"launch_window","line":5,"kind":"text","role":"loose","duplicate":false,"diagnostic":""},{"key":"
failed  exit=1  duration=1091146ms

