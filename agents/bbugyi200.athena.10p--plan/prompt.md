#gh:gh_bobs-org__bob-cli The `just install` command just failing on my mac machine for the bob-mac-capture project (see the command output below for context). Can you help me diagnose the root cause of this issue and fix it? #plan %m:@xlarge %auto
```
./Scripts/install.sh --target "/Users/bbugyi/Applications" --identity ""
Generating a 2048 bit RSA private key
..........................................................................................................................................................+++++
.+++++
writing new private key to '/var/folders/tp/10gl19wd7dxf1flq69dc3y0h0000gq/T/tmp.WW98bgd0wk/private-key.pem'
-----
Created "Bob Mac Capture Local" signing identity (SHA-1: F3F975F999F265DB2242731E643144B79AEE64C0).
The first signed install may show a codesign keychain prompt; choose Always Allow.
[1/1] Planning build
Building for production...
/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppDelegate.swift:797:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
795 |         openSettings: @escaping () -> Void = {},
796 |         activateApplication: @escaping () -> Void = {
797 |             NSApplication.shared.activate()
    |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
798 |         }
799 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 |

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppDelegate.swift:797:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
795 |         openSettings: @escaping () -> Void = {},
796 |         activateApplication: @escaping () -> Void = {
797 |             NSApplication.shared.activate()
    |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
798 |         }
799 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 |
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 |

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppDelegate.swift:76:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |         NSApplication.shared.addSceneRepresentation(representation)
 75 |         settingsSceneRepresentation = representation
 76 |         settingsPresentation = SettingsPresentation {
    |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |             representation.environment.openSettings()
 78 |         }
    :
792 |     var activateApplication: () -> Void
793 |
794 |     init(
    |     `- note: 'init(openSettings:activateApplication:)' declared here
795 |         openSettings: @escaping () -> Void = {},
796 |         activateApplication: @escaping () -> Void = {

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppDelegate.swift:269:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
267 |         menu.addItem(redo)
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
271 |         menu.addItem(

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppDelegate.swift:270:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
271 |         menu.addItem(
272 |             NSMenuItem(

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppDelegate.swift:278:62: warning: use '#selector' instead of explicitly constructing a 'Selector'
276 |             )
277 |         )
278 |         menu.addItem(NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                                              `- warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |         return menu
280 |     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppDelegate.swift:472:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
470 |     /// off MainActor state.
471 |     nonisolated static func storedHighlightsAppPath() -> String {
472 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |     }
474 |

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 |
 11 |     @Published var bobExecutableOverride: String {

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppDelegate.swift:542:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
540 |             library: library,
541 |             opener: WorkspaceRefsOpener(),
542 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
543 |             tabs: tabsSession,
544 |             isAdHocSigned: { signingState == .adHoc }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppDelegate.swift:704:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
702 |             return
703 |         }
704 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
705 |     }
706 |

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 |
 11 |     @Published var bobExecutableOverride: String {
    :
186 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
187 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
188 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
189 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
190 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CaptureAgendaView.swift:1050:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1048 |         for segment in parsed.segments {
1049 |             let slice = String(chars[segment.range])
1050 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1051 |         }
1052 |         return result.font(base).foregroundStyle(color)

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 |
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:1660:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1658 |                         requirePullInChoice: selection == nil,
1659 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1660 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1661 |                     )
1662 |                 }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:1660:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1658 |                         requirePullInChoice: selection == nil,
1659 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1660 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1661 |                     )
1662 |                 }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:6994:23: warning: no 'async' operations occur within 'await' expression
6992 |                 }
6993 |
6994 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
6995 |                     return
6996 |                 }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:6999:21: warning: no 'async' operations occur within 'await' expression
6997 |
6998 |                 if pickerNeeded == nil {
6999 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7000 |                         draft: draft,
7001 |                         previewDraft: closePending?.trimmed ?? draft,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:7013:27: warning: no 'async' operations occur within 'await' expression
7011 |                     await completionGate.value
7012 |                     try Task.checkCancellation()
7013 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7014 |                         return
7015 |                     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:7020:20: warning: no 'async' operations occur within 'await' expression
7018 |                 if let cursorUTF8Offset,
7019 |                    requestCompletion,
7020 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7021 |                        parse: parse,
7022 |                        cursor: cursorUTF8Offset,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:7026:37: warning: no 'async' operations occur within 'await' expression
7024 |                    ) == true
7025 |                 {
7026 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7027 |                         parse: parse,
7028 |                         cursor: cursorUTF8Offset,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:7232:28: warning: no 'async' operations occur within 'await' expression
7230 |         Task { [weak self, processClient] in
7231 |             do {
7232 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7233 |                 let processClientIdentity = processClient.identityToken
7234 |                 let preview = try await CaptureSignpost.measure("preview") {

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 |
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:149:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
147 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
148 |         }
149 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
150 |     }
151 |

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsLibrary.swift:722:20: warning: no 'async' operations occur within 'await' expression
720 |         ]
721 |         let watcher = VaultTargetWatcher(paths: paths, latency: 0.5) { [weak self] in
722 |             Task { await self?.handleWatcherChange() }
    |                    `- warning: no 'async' operations occur within 'await' expression
723 |         } onFailure: { [weak self] message in
724 |             Task { await self?.watcherFailed(message) }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsLibrary.swift:724:20: warning: no 'async' operations occur within 'await' expression
722 |             Task { await self?.handleWatcherChange() }
723 |         } onFailure: { [weak self] message in
724 |             Task { await self?.watcherFailed(message) }
    |                    `- warning: no 'async' operations occur within 'await' expression
725 |         }
726 |         self.watcher = watcher

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsListView.swift:173:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
171 |             .opacity(dimRows ? 0.6 : 1)
172 |             .onGeometryChange(for: CGRect?.self) { proxy in
173 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
174 |                     ? proxy.frame(in: .named("refsPanel")) : nil
175 |             } action: { rect in

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:259:40: note: property declared here
 257 |     /// The latest ranked tab rows, keyed by listing row id.
 258 |     @Published public private(set) var tabsListing: RefsTabsListing?
 259 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 260 |         didSet {
 261 |             if oldValue != selectedID {

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:169:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 167 |         completion: @escaping (Error?) -> Void
 168 |     ) {
 169 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 170 |         configuration.activates = true
 171 |         NSWorkspace.shared.open(

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:192:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 190 |
 191 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 192 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 193 |         configuration.activates = true
 194 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:475:20: warning: no 'async' operations occur within 'await' expression
 473 |         }.store(in: &subscriptions)
 474 |         let itemsSubscription = library.$items.sink { [weak self] _ in
 475 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 476 |         }
 477 |         let signalsSubscription = library.$signals.sink { [weak self] _ in

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:478:20: warning: no 'async' operations occur within 'await' expression
 476 |         }
 477 |         let signalsSubscription = library.$signals.sink { [weak self] _ in
 478 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 479 |         }
 480 |         itemsSubscription.store(in: &subscriptions)

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:483:20: warning: no 'async' operations occur within 'await' expression
 481 |         signalsSubscription.store(in: &subscriptions)
 482 |         library.$scanState.sink { [weak self] _ in
 483 |             Task { await self?.scanStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 484 |         }.store(in: &subscriptions)
 485 |         library.$refreshState.sink { [weak self] _ in

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:486:20: warning: no 'async' operations occur within 'await' expression
 484 |         }.store(in: &subscriptions)
 485 |         library.$refreshState.sink { [weak self] _ in
 486 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 487 |         }.store(in: &subscriptions)
 488 |     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:1897:13: warning: result of call to 'openSelected' is unused [#no-usage]
1895 |             openWithDefaultApp(item)
1896 |         case .note, .reveal:
1897 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
1898 |         }
1899 |     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:1938:17: warning: no 'async' operations occur within 'await' expression
1936 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
1937 |             Task {
1938 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
1939 |                     itemID: item.id,
1940 |                     title: item.title.text,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:1969:17: warning: no 'async' operations occur within 'await' expression
1967 |         opener.openWithDefaultApp(pdf) { [weak self] error in
1968 |             Task {
1969 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
1970 |                     itemID: item.id,
1971 |                     title: item.title.text,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/SettingsView.swift:342:34: error: cannot find type 'BobClientError' in scope
340 |                     ? "Templates cleared"
341 |                     : (response.error ?? "Templates could not be cleared")
342 |             } catch let error as BobClientError {
    |                                  `- error: cannot find type 'BobClientError' in scope
343 |                 if case .unsupportedCommand = error {
344 |                     savedTemplateShelf.refresh(reason: .recheck)

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>

error: recipe `install` failed on line 40 with exit code 1
```