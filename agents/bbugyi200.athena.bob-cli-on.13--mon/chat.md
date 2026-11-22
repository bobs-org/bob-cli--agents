# Chat History - ace-run (bob-cli-on.13--mon)

- **TIMESTAMP:** 2026-11-22 07:50:06 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-on.13--mon

## Prompt

sase monitor start --command "ssh -o BatchMode=yes -o ConnectTimeout=5 mac /tmp/bob-mac-capture-on13.aCPFV1/Scripts/bundle.sh --output /tmp/bob-mac-capture-on13.aCPFV1/.build/bundle '&&' ssh -o BatchMode=yes -o ConnectTimeout=5 mac /tmp/bob-mac-capture-on13.aCPFV1/Scripts/typecheck-tests.sh" --reason 'Compile the Bob Mac Capture app and type-check its Mac test targets for bob-cli-on.13'

## Response

sase: running unwrapped (no profile (monitor.tool_wrap is verify))
[0/1] Planning build
Building for production...
[0/3] Write sources
[1/3] Write swift-version--1AB21518FC5DEDBE.txt
[3/4] Compiling BobMacCapture AccessibilityTrust.swift
/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/AppDelegate.swift:1189:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1187 |         openSettings: @escaping () -> Void = {},
1188 |         activateApplication: @escaping () -> Void = {
1189 |             NSApplication.shared.activate()
     |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1190 |         }
1191 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/AppDelegate.swift:1189:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1187 |         openSettings: @escaping () -> Void = {},
1188 |         activateApplication: @escaping () -> Void = {
1189 |             NSApplication.shared.activate()
     |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1190 |         }
1191 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/AppDelegate.swift:93:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  91 |         NSApplication.shared.addSceneRepresentation(representation)
  92 |         settingsSceneRepresentation = representation
  93 |         settingsPresentation = SettingsPresentation {
     |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  94 |             representation.environment.openSettings()
  95 |         }
     :
1184 |     var activateApplication: () -> Void
1185 | 
1186 |     init(
     |     `- note: 'init(openSettings:activateApplication:)' declared here
1187 |         openSettings: @escaping () -> Void = {},
1188 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CaptureAgendaStore.swift:84:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         processClient: BobProcessClient? = nil,
 83 |         vaultRootPath: String = "",
 84 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 85 |         now: @Sendable @escaping () -> Date = { Date() },
 86 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/WalkAttentionStore.swift:68:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 66 |         processClient: BobProcessClient? = nil,
 67 |         vaultRootPath: String = "",
 68 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 69 |         now: @Sendable @escaping () -> Date = { Date() },
 70 |         debounceInterval: @Sendable @escaping (Bool) -> TimeInterval = {

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/AppDelegate.swift:379:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 377 |         menu.addItem(redo)
 378 |         menu.addItem(.separator())
 379 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 380 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 381 |         menu.addItem(

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/AppDelegate.swift:380:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 378 |         menu.addItem(.separator())
 379 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 380 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 381 |         menu.addItem(
 382 |             NSMenuItem(

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/AppDelegate.swift:389:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 387 |         )
 388 |         menu.addItem(
 389 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 390 |         return menu
 391 |     }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/AppDelegate.swift:696:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 694 |     /// off MainActor state.
 695 |     nonisolated static func storedHighlightsAppPath() -> String {
 696 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 697 |     }
 698 | 

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/AppDelegate.swift:776:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 774 |             library: library,
 775 |             opener: WorkspaceRefsOpener(),
 776 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 777 |             tabs: tabsSession,
 778 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/AppDelegate.swift:1079:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
1077 |             return
1078 |         }
1079 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1080 |     }
1081 | 

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/AppSettings.swift:282:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
280 |     static let refsHighlightsCodeKey = "refsHighlightsCodeKey"
281 |     static let refsHighlightsLinkKey = "refsHighlightsLinkKey"
282 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
283 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
284 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CaptureAgendaStore.swift:422:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
420 |                 Task { [weak self] in
421 |                     await MainActor.run {
422 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
423 |                     }
424 |                 }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CaptureAgendaView.swift:1689:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1687 |         for segment in parsed.segments {
1688 |             let slice = String(chars[segment.range])
1689 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1690 |         }
1691 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelController.swift:1880:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1878 |         }
1879 | 
1880 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1881 |         return true
1882 |     }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelController.swift:3961:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
3959 |         }
3960 |         if let textView = firstResponder as? NSTextView,
3961 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
3962 |            field.accessibilityIdentifier() == identifier
3963 |         {

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelModel.swift:4495:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 4493 |                         requireInboxRouteChoice: true,
 4494 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 4495 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil,
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 4496 |                         expectPastWindows: expectPastWindows
 4497 |                     )

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelModel.swift:4495:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 4493 |                         requireInboxRouteChoice: true,
 4494 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 4495 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil,
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 4496 |                         expectPastWindows: expectPastWindows
 4497 |                     )

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelModel.swift:5089:13: warning: initialization of immutable value 'requestID' was never used; consider replacing with assignment to '_' or removing it [#no-usage]
 5087 |         statusText = "Refreshing successor offers…"
 5088 |         let generation = analysisGeneration
 5089 |         let requestID = UUID()
      |             `- warning: initialization of immutable value 'requestID' was never used; consider replacing with assignment to '_' or removing it [#no-usage]
 5090 |         Task { [weak self, processClient] in
 5091 |             do {

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelModel.swift:5534:20: warning: result of call to 'armEscDiscard()' is unused [#no-usage]
 5532 |         // Two-step Esc while verdicts are staged.
 5533 |         if choice.closeCount > 0, !choice.outcomes.isEscArmed {
 5534 |             choice.armEscDiscard()
      |                    `- warning: result of call to 'armEscDiscard()' is unused [#no-usage]
 5535 |             pullInChoice = choice
 5536 |             let text = choice.outcomes.escArmedText ?? "Esc again to discard closes"

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelModel.swift:12818:33: warning: implicit use of 'self' in closure; use 'self.' to make capture semantics explicit; this is an error in the Swift 6 language mode
12816 |                             source: .noteGoto,
12817 |                             index: .noteGoto(
12818 |                                 makeNoteGotoIndex(candidates: candidates, noteGoto: noteGoto)
      |                                 `- warning: implicit use of 'self' in closure; use 'self.' to make capture semantics explicit; this is an error in the Swift 6 language mode
12819 |                             ),
12820 |                             candidates: candidates,

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelModel.swift:15690:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
15688 |         newName: String
15689 |     ) {
15690 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
15691 |               let rename = current.rename,
15692 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelModel.swift:19931:27: warning: result of call to 'failGotoScopeSwapIfTarget()' is unused [#no-usage]
19929 |                         return
19930 |                     }
19931 |                     self?.failGotoScopeSwapIfTarget()
      |                           `- warning: result of call to 'failGotoScopeSwapIfTarget()' is unused [#no-usage]
19932 |                     self?.previewState = .failed(String(describing: error))
19933 |                 }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelModel.swift:19778:23: warning: no 'async' operations occur within 'await' expression
19776 |                 }
19777 | 
19778 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
19779 |                     return
19780 |                 }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelModel.swift:19791:35: warning: no 'async' operations occur within 'await' expression
19789 |                         CaptureGrammarGate.isCompatible(parse.grammar)
19790 |                         && parse.reportsClipDirective
19791 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
19792 |                         draft: draft,
19793 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelModel.swift:19806:27: warning: no 'async' operations occur within 'await' expression
19804 |                     await completionGate.value
19805 |                     try Task.checkCancellation()
19806 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
19807 |                         return
19808 |                     }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelModel.swift:19816:47: warning: no 'async' operations occur within 'await' expression
19814 |                     shouldRequestCompletion = true
19815 |                 } else if let cursorUTF8Offset, requestCompletion {
19816 |                     shouldRequestCompletion = await self?.shouldRequestCompletion(
      |                                               `- warning: no 'async' operations occur within 'await' expression
19817 |                         parse: parse,
19818 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelModel.swift:19840:37: warning: no 'async' operations occur within 'await' expression
19838 |                         return
19839 |                     }
19840 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
19841 |                         parse: parse,
19842 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelModel.swift:23933:19: warning: variable 'request' was never mutated; consider changing to 'let' constant
23931 |             )
23932 |         }
23933 |         guard var request = aliasTipRequest,
      |                   `- warning: variable 'request' was never mutated; consider changing to 'let' constant
23934 |             request.generation == generation,
23935 |             request.anchor.draft == draft

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelModel.swift:24134:19: warning: value 'pending' was defined but never used; consider replacing with boolean test [#no-usage]
24132 |     ) {
24133 |         presentedAliasTip = nil
24134 |         guard let pending = pendingAliasTip else {
      |                   `- warning: value 'pending' was defined but never used; consider replacing with boolean test [#no-usage]
24135 |             if var request = aliasTipRequest, request.openedSurface == nil {
24136 |                 request.dropReason = reason

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelView.swift:3128:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3126 |         return Text(String(label[..<range.lowerBound]))
3127 |             + Text(String(label[range])).bold()
3128 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3129 |     }
3130 | 

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelView.swift:3127:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3125 |         }
3126 |         return Text(String(label[..<range.lowerBound]))
3127 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3128 |             + Text(String(label[range.upperBound...]))
3129 |     }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelView.swift:3971:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3969 |                     + Text("●").foregroundStyle(
3970 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3971 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3972 |                     .font(.caption)
3973 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePanelView.swift:3969:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3967 |             if parts.count == 2 {
3968 |                 (Text(parts[0]).foregroundStyle(.secondary)
3969 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3970 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3971 |                     + Text(parts[1]).foregroundStyle(.secondary))

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePickerView.swift:1254:33: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1252 |         if !label.isEmpty {
1253 |             if hasContent {
1254 |                 result = result + Text(" · ")
     |                                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1255 |             }
1256 |             result = result + Text(Image(systemName: icon)) + Text(" \(label)")

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePickerView.swift:1256:61: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1254 |                 result = result + Text(" · ")
1255 |             }
1256 |             result = result + Text(Image(systemName: icon)) + Text(" \(label)")
     |                                                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1257 |             hasContent = true
1258 |         }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePickerView.swift:1256:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1254 |                 result = result + Text(" · ")
1255 |             }
1256 |             result = result + Text(Image(systemName: icon)) + Text(" \(label)")
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1257 |             hasContent = true
1258 |         }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePickerView.swift:1260:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1258 |         }
1259 |         if let section = row.detail.section, !section.isEmpty {
1260 |             result = result + Text(" › \(section)")
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1261 |             hasContent = true
1262 |         }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePickerView.swift:1265:33: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1263 |         if !row.detail.summary.isEmpty {
1264 |             if hasContent {
1265 |                 result = result + Text(" · ")
     |                                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1266 |             }
1267 |             result = result + Text(row.detail.summary)

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePickerView.swift:1267:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1265 |                 result = result + Text(" · ")
1266 |             }
1267 |             result = result + Text(row.detail.summary)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1268 |         }
1269 |         return result

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePullInChoiceView.swift:986:19: warning: immutable value 'key' was never used; consider replacing with '_' or removing it [#no-usage]
 984 | 
 985 |     private var cancelDetailText: (text: String, faint: Bool)? {
 986 |         guard let key = offerKey, case .cancel(let reason) = verdict else {
     |                   `- warning: immutable value 'key' was never used; consider replacing with '_' or removing it [#no-usage]
 987 |             return nil
 988 |         }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePullInChoiceView.swift:1053:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1051 |             let chunk = Text("\(separator)\(entry.element.text)")
1052 |                 .foregroundStyle(entry.element.tint ?? .secondary)
1053 |             return result + chunk
     |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1054 |         }
1055 |     }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePullInLinkBand.swift:283:17: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
281 |         if content.locatorIsSuggestion {
282 |             return Text("⊕ ").foregroundStyle(.tertiary) + head + delimiter
283 |                 + Text(id).italic().foregroundStyle(.tertiary)
    |                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
284 |         }
285 |         return head + delimiter

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePullInLinkBand.swift:282:67: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
280 |         guard let id = content.locatorID else { return head }
281 |         if content.locatorIsSuggestion {
282 |             return Text("⊕ ").foregroundStyle(.tertiary) + head + delimiter
    |                                                                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
283 |                 + Text(id).italic().foregroundStyle(.tertiary)
284 |         }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePullInLinkBand.swift:282:60: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
280 |         guard let id = content.locatorID else { return head }
281 |         if content.locatorIsSuggestion {
282 |             return Text("⊕ ").foregroundStyle(.tertiary) + head + delimiter
    |                                                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
283 |                 + Text(id).italic().foregroundStyle(.tertiary)
284 |         }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePullInLinkBand.swift:286:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
284 |         }
285 |         return head + delimiter
286 |             + Text(id).foregroundStyle(CaptureEditorPalette.color(for: .blockID))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
287 |     }
288 | 

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePullInLinkBand.swift:285:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
283 |                 + Text(id).italic().foregroundStyle(.tertiary)
284 |         }
285 |         return head + delimiter
    |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
286 |             + Text(id).foregroundStyle(CaptureEditorPalette.color(for: .blockID))
287 |     }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePullInLinkBand.swift:417:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
415 |             .foregroundStyle(Color.accentColor)
416 |             .fontWeight(.semibold)
417 |             + Text(after)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
418 |     }
419 | 

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePullInLinkBand.swift:414:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
412 |         let after = String(primary[upper..<primary.endIndex])
413 |         return Text(before)
414 |             + Text(hit)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
415 |             .foregroundStyle(Color.accentColor)
416 |             .fontWeight(.semibold)

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePullInRecallBand.swift:165:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
163 |             .foregroundStyle(Color.accentColor)
164 |             .fontWeight(.semibold)
165 |             + Text(after)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
166 |             .foregroundStyle(isSelected ? Color.primary : Color.secondary)
167 |     }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CapturePullInRecallBand.swift:162:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
160 |         return Text(before)
161 |             .foregroundStyle(isSelected ? Color.primary : Color.secondary)
162 |             + Text(hit)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
163 |             .foregroundStyle(Color.accentColor)
164 |             .fontWeight(.semibold)

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/CaptureTransferFailureCardView.swift:129:17: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
127 |             result =
128 |                 result
129 |                 + Text(String(characters[lower..<upper]))
    |                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
130 |                 .foregroundColor(formColor(segment.part))
131 |         }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
179 | @MainActor
180 | public final class RefsDecodedImageBudget {
181 |     public static let defaultByteLimit = RefsAnnotationImageLoader.bitmapCacheByteLimit
    |                       `- note: static property declared here
182 | 
183 |     private let byteLimit: Int
    :
186 |     public private(set) var byteCost = 0
187 | 
188 |     public init(byteLimit: Int = defaultByteLimit) {
    |                                  `- warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
189 |         self.byteLimit = max(byteLimit, 1)
190 |     }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,

/private/tmp/bob-mac-capture-on13.aCPFV1/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[3/5] Write Objects.LinkFileList
[4/5] Linking BobMacCapture
Build of product 'BobMacCapture' complete! (100.31s)
/tmp/bob-mac-capture-on13.aCPFV1/.build/bundle/Bob Mac Capture.app/Contents/MacOS/BobMacCapture: replacing existing signature
/tmp/bob-mac-capture-on13.aCPFV1/.build/bundle/Bob Mac Capture.app: replacing existing signature
/tmp/bob-mac-capture-on13.aCPFV1/.build/bundle/Bob Mac Capture.app
Host key verification failed.

