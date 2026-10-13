- **PLAN:**
  [202610/mac_capture_install_compile_fix.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_capture_install_compile_fix.md)
- **AGENTS:**
  - [bbugyi200.athena.101--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.101.md)

Can you help me fix the bob-mac-capture app's `just install` command (see the command
output below for context)? Think this through thoroughly and create a plan using your
`/sase_plan` skill. Choose and author the appropriate tier, validate and revalidate
until it passes, then submit it with `sase plan propose` (as the skill instructs) before
making any file changes.

```
/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:2097:45: error: value of optional type 'String?' must be unwrapped to a value of type 'String'
2095 |                 trigger: trigger,
2096 |                 source: completion.context == "task_goto" ? .taskGoto : .taskLink,
2097 |                 expectedContext: completion.context
     |                                             |- error: value of optional type 'String?' must be unwrapped to a value of type 'String'
     |                                             |- note: coalesce using '??' to provide a default when the optional value contains 'nil'
     |                                             `- note: force-unwrap using '!' to abort execution if the optional value contains 'nil'
2098 |             )
2099 |             return

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:5703:23: warning: no 'async' operations occur within 'await' expression
5701 |                 }
5702 |
5703 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
5704 |                     return
5705 |                 }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:5708:21: warning: no 'async' operations occur within 'await' expression
5706 |
5707 |                 if pickerNeeded == nil {
5708 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
5709 |                         draft: draft,
5710 |                         previewDraft: closePending?.trimmed ?? draft,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:5722:27: warning: no 'async' operations occur within 'await' expression
5720 |                     await completionGate.value
5721 |                     try Task.checkCancellation()
5722 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
5723 |                         return
5724 |                     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:5729:20: warning: no 'async' operations occur within 'await' expression
5727 |                 if let cursorUTF8Offset,
5728 |                    requestCompletion,
5729 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
5730 |                        parse: parse,
5731 |                        cursor: cursorUTF8Offset,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:5735:37: warning: no 'async' operations occur within 'await' expression
5733 |                    ) == true
5734 |                 {
5735 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
5736 |                         parse: parse,
5737 |                         cursor: cursorUTF8Offset,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:5941:28: warning: no 'async' operations occur within 'await' expression
5939 |         Task { [weak self, processClient] in
5940 |             do {
5941 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
5942 |                 let preview = try await CaptureSignpost.measure("preview") {
5943 |                     try await processClient.captureLivePreview(

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:140:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
138 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
139 |         }
140 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
141 |     }
142 |

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsLibrary.swift:655:20: warning: no 'async' operations occur within 'await' expression
653 |         ]
654 |         let watcher = VaultTargetWatcher(paths: paths, latency: 0.5) { [weak self] in
655 |             Task { await self?.handleWatcherChange() }
    |                    `- warning: no 'async' operations occur within 'await' expression
656 |         } onFailure: { [weak self] message in
657 |             Task { await self?.watcherFailed(message) }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsLibrary.swift:657:20: warning: no 'async' operations occur within 'await' expression
655 |             Task { await self?.handleWatcherChange() }
656 |         } onFailure: { [weak self] message in
657 |             Task { await self?.watcherFailed(message) }
    |                    `- warning: no 'async' operations occur within 'await' expression
658 |         }
659 |         self.watcher = watcher

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsListView.swift:169:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
167 |             )
168 |             .onGeometryChange(for: CGRect?.self) { proxy in
169 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
170 |                     ? proxy.frame(in: .named("refsPanel")) : nil
171 |             } action: { rect in

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:196:40: note: property declared here
 194 |     @Published public private(set) var scope: RefScope = .all
 195 |     @Published public private(set) var listing: RefsListing
 196 |     @Published public private(set) var selectedID: String?
     |                                        `- note: property declared here
 197 |     @Published public private(set) var unavailableIDs: Set<String> = []
 198 |     @Published public private(set) var banner: RefsBanner?

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:127:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 125 |         completion: @escaping (Error?) -> Void
 126 |     ) {
 127 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 128 |         configuration.activates = true
 129 |         NSWorkspace.shared.open(

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:150:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 148 |
 149 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 150 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 151 |         configuration.activates = true
 152 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:286:20: warning: no 'async' operations occur within 'await' expression
 284 |         }.store(in: &subscriptions)
 285 |         let itemsSubscription = library.$items.sink { [weak self] _ in
 286 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 287 |         }
 288 |         let signalsSubscription = library.$signals.sink { [weak self] _ in

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:20: warning: no 'async' operations occur within 'await' expression
 287 |         }
 288 |         let signalsSubscription = library.$signals.sink { [weak self] _ in
 289 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 290 |         }
 291 |         itemsSubscription.store(in: &subscriptions)

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:294:20: warning: no 'async' operations occur within 'await' expression
 292 |         signalsSubscription.store(in: &subscriptions)
 293 |         library.$scanState.sink { [weak self] _ in
 294 |             Task { await self?.scanStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 295 |         }.store(in: &subscriptions)
 296 |     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:711:13: warning: no 'async' operations occur within 'await' expression
 709 |                 return
 710 |             }
 711 |             await self?.clearToast()
     |             `- warning: no 'async' operations occur within 'await' expression
 712 |         }
 713 |     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:925:13: warning: result of call to 'openSelected' is unused [#no-usage]
 923 |             openWithDefaultApp(item)
 924 |         case .note, .reveal:
 925 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
 926 |         }
 927 |     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:952:17: warning: no 'async' operations occur within 'await' expression
 950 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
 951 |             Task {
 952 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
 953 |                     itemID: item.id,
 954 |                     title: item.title.text,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:976:17: warning: no 'async' operations occur within 'await' expression
 974 |         opener.openWithDefaultApp(pdf) { [weak self] error in
 975 |             Task {
 976 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
 977 |                     itemID: item.id,
 978 |                     title: item.title.text,

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>

error: recipe `install` failed on line 22 with exit code 1
  ✗ up to date · 7b87f79 · install failed (exit 1)
```
