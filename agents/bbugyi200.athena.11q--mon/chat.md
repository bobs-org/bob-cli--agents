# Chat History - ace-run (11q--mon)

- **TIMESTAMP:** 2026-10-19 09:58:39 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** 11q--mon

## Prompt

sase monitor start --command 'set -eu; scratch_path="/tmp/bob-refs-panel-latency-$(date +%s)-$$"; ssh -o BatchMode=yes -o ConnectTimeout=10 mac "mkdir -p \\"$scratch_path\\""; rsync -a --exclude=.build/ --exclude=.git/ ./ "mac:$scratch_path/"; remote_command="set -eu; cd \\"$scratch_path\\"; trap \'rm -rf \\"$scratch_path\\"\' EXIT; Scripts/bundle.sh; just typecheck-tests"; ssh -o BatchMode=yes -o ConnectTimeout=10 mac "$remote_command"' --reason 'Compile the approved Refs latency changes on the Mac scratch copy'

## Response

sase tool run 01c39a5fbeb2b9bc489cd8828b5db2cd
X11 forwarding request failed on channel 0
X11 forwarding request failed on channel 0
Building for production...
[0/6] Write sources
[3/6] Write swift-version--1AB21518FC5DEDBE.txt
[5/7] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 2 | 
 3 | public struct BobExecutableResolver: Sendable {
 4 |     public let fileManager: FileManager
   |                `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 5 |     public let homeDirectory: URL
 6 |     public let candidates: [String]

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 | 
 45 |     private let fileURL: URL
 46 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 47 |     private let onError: @Sendable (String) -> Void
 48 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/DependencyPickerPresentation.swift:486:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
484 | /// locator stays searchable.
485 | private struct DependencyPickerIndexEntry: Sendable {
486 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
487 |     let bobIndex: Int
488 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[6/8] Compiling RefsCore RefsCaption.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 41 | 
 42 |   private let fileURL: URL
 43 |   private let fileManager: FileManager
    |               `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 |   private let onError: @Sendable (String) -> Void
 45 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
182 | 
183 |   private let fileURL: URL
184 |   private let fileManager: FileManager
    |               `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
185 |   private let onError: @Sendable (String) -> Void
186 |   private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[7/9] Compiling BobMacCapture AccessibilityTrust.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
811 |         }
812 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
811 |         }
812 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:76:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |         NSApplication.shared.addSceneRepresentation(representation)
 75 |         settingsSceneRepresentation = representation
 76 |         settingsPresentation = SettingsPresentation {
    |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |             representation.environment.openSettings()
 78 |         }
    :
805 |     var activateApplication: () -> Void
806 | 
807 |     init(
    |     `- note: 'init(openSettings:activateApplication:)' declared here
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:269:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
267 |         menu.addItem(redo)
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
271 |         menu.addItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:270:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
271 |         menu.addItem(
272 |             NSMenuItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:278:62: warning: use '#selector' instead of explicitly constructing a 'Selector'
276 |             )
277 |         )
278 |         menu.addItem(NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                                              `- warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |         return menu
280 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:472:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
470 |     /// off MainActor state.
471 |     nonisolated static func storedHighlightsAppPath() -> String {
472 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |     }
474 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:542:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
540 |             library: library,
541 |             opener: WorkspaceRefsOpener(),
542 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
543 |             tabs: tabsSession,
544 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:717:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
715 |             return
716 |         }
717 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
718 |     }
719 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:149:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
147 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
148 |         }
149 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
150 |     }
151 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:476:27: warning: expression of type 'Bool' is unused [#no-usage]
474 |     private func refreshSnapshotAfterRename() async {
475 |         while let current = snapshotTask {
476 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
477 |         }
478 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:480:27: warning: expression of type 'Bool' is unused [#no-usage]
478 |         refreshSnapshot(reason: .manual)
479 |         while let current = snapshotTask {
480 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
481 |         }
482 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:737:27: warning: expression of type 'Bool' is unused [#no-usage]
735 |     private func runPostScanRefresh() async {
736 |         while let current = snapshotTask {
737 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
738 |             if snapshotTask == nil {
739 |                 break

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:744:27: warning: expression of type 'Bool' is unused [#no-usage]
742 |         refresh(reason: .scan)
743 |         while let current = snapshotTask {
744 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
745 |             if snapshotTask == nil {
746 |                 break

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:806:24: warning: no 'async' operations occur within 'await' expression
804 |                     return
805 |                 }
806 |                 Task { await self?.handleWatcherChange() }
    |                        `- warning: no 'async' operations occur within 'await' expression
807 |             },
808 |             onFailure: { [weak self] message in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:809:24: warning: no 'async' operations occur within 'await' expression
807 |             },
808 |             onFailure: { [weak self] message in
809 |                 Task { await self?.watcherFailed(message) }
    |                        `- warning: no 'async' operations occur within 'await' expression
810 |             }
811 |         )

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsListView.swift:189:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
187 |                 // rows report nil, which never clears the current rect.
188 |                 .onGeometryChange(for: CGRect?.self) { proxy in
189 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
190 |                         ? proxy.frame(in: .named("refsPanel")) : nil
191 |                 } action: { rect in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:287:40: note: property declared here
 285 |         return tabsFilter && tabsListing?.tabs[id] != nil
 286 |     }
 287 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 288 |         didSet {
 289 |             if oldValue != selectedID {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsListView.swift:227:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
225 |             .transition(removalTransition)
226 |             .onGeometryChange(for: CGRect?.self) { proxy in
227 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
228 |                     ? proxy.frame(in: .named("refsPanel")) : nil
229 |             } action: { rect in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:287:40: note: property declared here
 285 |         return tabsFilter && tabsListing?.tabs[id] != nil
 286 |     }
 287 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 288 |         didSet {
 289 |             if oldValue != selectedID {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:181:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 179 |         completion: @escaping (Error?) -> Void
 180 |     ) {
 181 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 182 |         configuration.activates = true
 183 |         NSWorkspace.shared.open(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:204:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 202 | 
 203 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 204 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 205 |         configuration.activates = true
 206 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:554:20: warning: no 'async' operations occur within 'await' expression
 552 |         }.store(in: &subscriptions)
 553 |         let itemsSubscription = library.$items.sink { [weak self] _ in
 554 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 555 |         }
 556 |         let signalsSubscription = library.$signals.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:557:20: warning: no 'async' operations occur within 'await' expression
 555 |         }
 556 |         let signalsSubscription = library.$signals.sink { [weak self] _ in
 557 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 558 |         }
 559 |         itemsSubscription.store(in: &subscriptions)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:562:20: warning: no 'async' operations occur within 'await' expression
 560 |         signalsSubscription.store(in: &subscriptions)
 561 |         library.$todayRefreshGeneration.sink { [weak self] _ in
 562 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 563 |         }.store(in: &subscriptions)
 564 |         library.$scanState.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:565:20: warning: no 'async' operations occur within 'await' expression
 563 |         }.store(in: &subscriptions)
 564 |         library.$scanState.sink { [weak self] _ in
 565 |             Task { await self?.scanStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 566 |         }.store(in: &subscriptions)
 567 |         library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:568:20: warning: no 'async' operations occur within 'await' expression
 566 |         }.store(in: &subscriptions)
 567 |         library.$refreshState.sink { [weak self] _ in
 568 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 569 |         }.store(in: &subscriptions)
 570 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2648:13: warning: result of call to 'openSelected' is unused [#no-usage]
2646 |             openWithDefaultApp(item)
2647 |         case .note, .reveal:
2648 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
2649 |         }
2650 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2680:17: warning: no 'async' operations occur within 'await' expression
2678 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
2679 |             Task {
2680 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
2681 |             }
2682 |         }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2707:17: warning: no 'async' operations occur within 'await' expression
2705 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
2706 |             Task {
2707 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
2708 |             }
2709 |         }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2765:17: warning: no 'async' operations occur within 'await' expression
2763 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
2764 |             Task {
2765 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
2766 |                     itemID: item.id,
2767 |                     title: item.title.text,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2796:17: warning: no 'async' operations occur within 'await' expression
2794 |         opener.openWithDefaultApp(pdf) { [weak self] error in
2795 |             Task {
2796 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
2797 |                     itemID: item.id,
2798 |                     title: item.title.text,

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[7/9] Write Objects.LinkFileList
[8/9] Linking BobMacCapture
Build of product 'BobMacCapture' complete! (143.75s)
/tmp/bob-refs-panel-latency-1792418072-2997714/.build/bundle/Bob Mac Capture.app/Contents/MacOS/BobMacCapture: replacing existing signature
/tmp/bob-refs-panel-latency-1792418072-2997714/.build/bundle/Bob Mac Capture.app: replacing existing signature
/tmp/bob-refs-panel-latency-1792418072-2997714/.build/bundle/Bob Mac Capture.app
./Scripts/typecheck-tests.sh
Building for debugging...
[0/18] Write sources
[5/18] Write refs-rank-entitlement.plist
[6/18] Write BobMacCapture-entitlement.plist
[7/18] Write BobMacCaptureInstallHelper-entitlement.plist
[8/18] Write swift-version--1AB21518FC5DEDBE.txt
[10/73] Compiling CaptureCore CanceledDraftStashStore.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 | 
 45 |     private let fileURL: URL
 46 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 47 |     private let onError: @Sendable (String) -> Void
 48 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[11/73] Compiling CaptureCore CaptureAgendaFitPlanner.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 | 
 45 |     private let fileURL: URL
 46 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 47 |     private let onError: @Sendable (String) -> Void
 48 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[12/73] Compiling CaptureCore CaptureAgendaHold.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 | 
 45 |     private let fileURL: URL
 46 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 47 |     private let onError: @Sendable (String) -> Void
 48 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[13/73] Compiling CaptureCore CaptureAgendaInlineText.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 | 
 45 |     private let fileURL: URL
 46 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 47 |     private let onError: @Sendable (String) -> Void
 48 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[14/73] Compiling CaptureCore CaptureAgendaLayout.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 | 
 45 |     private let fileURL: URL
 46 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 47 |     private let onError: @Sendable (String) -> Void
 48 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[15/73] Compiling CaptureCore CaptureAgendaModels.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 | 
 45 |     private let fileURL: URL
 46 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 47 |     private let onError: @Sendable (String) -> Void
 48 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[16/73] Compiling CaptureCore CaptureAgendaPresentation.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 | 
 45 |     private let fileURL: URL
 46 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 47 |     private let onError: @Sendable (String) -> Void
 48 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[17/73] Compiling CaptureCore CaptureAgendaRefreshFilter.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 | 
 45 |     private let fileURL: URL
 46 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 47 |     private let onError: @Sendable (String) -> Void
 48 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[18/73] Compiling CaptureCore CapturePomodoroClosePresentation.swift
[19/73] Compiling CaptureCore CapturePomodoroLineTokens.swift
[20/73] Compiling CaptureCore CapturePomodoroLinkPresentation.swift
[21/73] Compiling CaptureCore CapturePomodoroResetPresentation.swift
[22/73] Compiling CaptureCore CapturePomodoroShiftPresentation.swift
[23/73] Compiling CaptureCore CapturePomodoroStartPresentation.swift
[24/73] Compiling CaptureCore CaptureProjectNotePresentation.swift
[25/73] Compiling CaptureCore CaptureRefFileUnder.swift
[26/80] Compiling CaptureCore CaptureRefPresentation.swift
[27/80] Compiling CaptureCore CaptureRelationshipCopy.swift
[28/80] Compiling CaptureCore CaptureRelationshipPresentation.swift
[29/80] Compiling CaptureCore CaptureSavedTemplates.swift
[30/80] Compiling CaptureCore CaptureSubBulletPresentation.swift
[31/80] Compiling CaptureCore CaptureSuccessorPresentation.swift
[32/80] Compiling CaptureCore CaptureTargetsCache.swift
[33/80] Compiling CaptureCore CaptureOpenHintPresentation.swift
[34/80] Compiling CaptureCore CaptureOpenPlan.swift
[35/80] Compiling CaptureCore CapturePanelPlacement.swift
[36/80] Compiling CaptureCore CapturePickerHelpers.swift
[37/80] Compiling CaptureCore CapturePickerPresentation.swift
[38/80] Compiling CaptureCore CapturePlanBudgetPresentation.swift
[39/80] Compiling CaptureCore CapturePomodoroAdjustPresentation.swift
[40/80] Compiling CaptureCore CapturePomodoroBlockPresentation.swift
[41/80] Compiling CaptureCore FuzzyMatcher.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[42/80] Compiling CaptureCore ObsidianOpenURL.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[43/80] Compiling CaptureCore ParentTaskPickerPresentation.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[44/80] Compiling CaptureCore PomodoroHomes.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[45/80] Compiling CaptureCore TaskCompletePickerPresentation.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[46/80] Compiling CaptureCore TaskDisplayText.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[47/80] Compiling CaptureCore TaskLinkPickerPresentation.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[48/80] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 2 | 
 3 | public struct BobExecutableResolver: Sendable {
 4 |     public let fileManager: FileManager
   |                `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 5 |     public let homeDirectory: URL
 6 |     public let candidates: [String]

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[49/80] Compiling CaptureCore BlockIDPickerIndex.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 2 | 
 3 | public struct BobExecutableResolver: Sendable {
 4 |     public let fileManager: FileManager
   |                `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 5 |     public let homeDirectory: URL
 6 |     public let candidates: [String]

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[50/80] Compiling CaptureCore BlockIDRules.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 2 | 
 3 | public struct BobExecutableResolver: Sendable {
 4 |     public let fileManager: FileManager
   |                `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 5 |     public let homeDirectory: URL
 6 |     public let candidates: [String]

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[51/80] Compiling CaptureCore BobEnvironment.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 2 | 
 3 | public struct BobExecutableResolver: Sendable {
 4 |     public let fileManager: FileManager
   |                `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 5 |     public let homeDirectory: URL
 6 |     public let candidates: [String]

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[52/80] Compiling CaptureCore BobErrors.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 2 | 
 3 | public struct BobExecutableResolver: Sendable {
 4 |     public let fileManager: FileManager
   |                `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 5 |     public let homeDirectory: URL
 6 |     public let candidates: [String]

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[53/80] Compiling CaptureCore BobExecutableResolver.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 2 | 
 3 | public struct BobExecutableResolver: Sendable {
 4 |     public let fileManager: FileManager
   |                `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 5 |     public let homeDirectory: URL
 6 |     public let candidates: [String]

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[54/80] Compiling CaptureCore BobMacCaptureLaunchContext.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 2 | 
 3 | public struct BobExecutableResolver: Sendable {
 4 |     public let fileManager: FileManager
   |                `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 5 |     public let homeDirectory: URL
 6 |     public let candidates: [String]

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[55/80] Compiling CaptureCore BobProcessClient.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 2 | 
 3 | public struct BobExecutableResolver: Sendable {
 4 |     public let fileManager: FileManager
   |                `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 5 |     public let homeDirectory: URL
 6 |     public let candidates: [String]

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[56/80] Compiling CaptureCore CaptureAgendaRefreshState.swift
[57/80] Compiling CaptureCore CaptureAgendaVisibility.swift
[58/80] Compiling CaptureCore CaptureBlockDiffRow.swift
[59/80] Compiling CaptureCore CaptureCloseTaskCommaAssist.swift
[60/80] Compiling CaptureCore CaptureCloseTaskCommaProvenance.swift
[61/80] Compiling CaptureCore CaptureEditWrite.swift
[62/80] Compiling CaptureCore CaptureLinkGuardPresentation.swift
[63/80] Compiling CaptureCore CaptureModels.swift
[64/80] Emitting module CaptureCore
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 2 | 
 3 | public struct BobExecutableResolver: Sendable {
 4 |     public let fileManager: FileManager
   |                `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 5 |     public let homeDirectory: URL
 6 |     public let candidates: [String]

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 | 
 45 |     private let fileURL: URL
 46 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 47 |     private let onError: @Sendable (String) -> Void
 48 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/DependencyPickerPresentation.swift:486:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
484 | /// locator stays searchable.
485 | private struct DependencyPickerIndexEntry: Sendable {
486 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
487 |     let bobIndex: Int
488 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[65/80] Compiling CaptureCore CaptureTaskBlockPresentation.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/DependencyPickerPresentation.swift:486:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
484 | /// locator stays searchable.
485 | private struct DependencyPickerIndexEntry: Sendable {
486 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
487 |     let bobIndex: Int
488 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[66/80] Compiling CaptureCore CaptureTaskCompletePresentation.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/DependencyPickerPresentation.swift:486:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
484 | /// locator stays searchable.
485 | private struct DependencyPickerIndexEntry: Sendable {
486 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
487 |     let bobIndex: Int
488 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[67/80] Compiling CaptureCore CaptureTextRanges.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/DependencyPickerPresentation.swift:486:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
484 | /// locator stays searchable.
485 | private struct DependencyPickerIndexEntry: Sendable {
486 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
487 |     let bobIndex: Int
488 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[68/80] Compiling CaptureCore CaptureTodayPomodoroGoto.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/DependencyPickerPresentation.swift:486:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
484 | /// locator stays searchable.
485 | private struct DependencyPickerIndexEntry: Sendable {
486 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
487 |     let bobIndex: Int
488 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[69/80] Compiling CaptureCore CaptureTogglePresentation.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/DependencyPickerPresentation.swift:486:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
484 | /// locator stays searchable.
485 | private struct DependencyPickerIndexEntry: Sendable {
486 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
487 |     let bobIndex: Int
488 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[70/80] Compiling CaptureCore CompletionRowContent.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/DependencyPickerPresentation.swift:486:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
484 | /// locator stays searchable.
485 | private struct DependencyPickerIndexEntry: Sendable {
486 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
487 |     let bobIndex: Int
488 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[71/80] Compiling CaptureCore DependencyPickerPresentation.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/DependencyPickerPresentation.swift:486:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
484 | /// locator stays searchable.
485 | private struct DependencyPickerIndexEntry: Sendable {
486 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
487 |     let bobIndex: Int
488 |     let display: TaskDisplayText

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[72/105] Emitting module RefsCore
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 41 | 
 42 |   private let fileURL: URL
 43 |   private let fileManager: FileManager
    |               `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 |   private let onError: @Sendable (String) -> Void
 45 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
182 | 
183 |   private let fileURL: URL
184 |   private let fileManager: FileManager
    |               `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
185 |   private let onError: @Sendable (String) -> Void
186 |   private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[73/107] Compiling RefsCore RefsSelection.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 41 | 
 42 |   private let fileURL: URL
 43 |   private let fileManager: FileManager
    |               `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 |   private let onError: @Sendable (String) -> Void
 45 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
182 | 
183 |   private let fileURL: URL
184 |   private let fileManager: FileManager
    |               `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
185 |   private let onError: @Sendable (String) -> Void
186 |   private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[74/107] Compiling RefsCore RefsStores.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 41 | 
 42 |   private let fileURL: URL
 43 |   private let fileManager: FileManager
    |               `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 |   private let onError: @Sendable (String) -> Void
 45 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
182 | 
183 |   private let fileURL: URL
184 |   private let fileManager: FileManager
    |               `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
185 |   private let onError: @Sendable (String) -> Void
186 |   private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[75/107] Compiling RefsCore RefsTabClose.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 41 | 
 42 |   private let fileURL: URL
 43 |   private let fileManager: FileManager
    |               `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 |   private let onError: @Sendable (String) -> Void
 45 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
182 | 
183 |   private let fileURL: URL
184 |   private let fileManager: FileManager
    |               `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
185 |   private let onError: @Sendable (String) -> Void
186 |   private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[76/107] Compiling RefsCore RefsTabsRanking.swift
[77/107] Compiling RefsCore RefsToday.swift
[78/107] Compiling RefsCore RefsFetching.swift
[79/107] Compiling RefsCore RefsHighlightPicker.swift
[80/107] Compiling RefsCore RefsHighlightsTabs.swift
[81/107] Compiling RefsCore RefsTodayLinkPresentation.swift
[82/107] Compiling RefsCore RefsWatcherRelevance.swift
[83/107] Compiling RefsCore RefsTodayLinkCard.swift
[84/107] Compiling RefsCore RefsTodayLinkModels.swift
[85/107] Compiling RefsCore RefsInspector.swift
[86/107] Compiling RefsCore RefsModel.swift
[87/107] Compiling RefsCore RefsNewest.swift
[88/107] Compiling RefsCore RefsCaption.swift
[89/107] Compiling RefsCore RefsCopy.swift
[90/107] Compiling RefsCore RefsDecoding.swift
[91/107] Compiling RefsCore RefsRanking.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {
[92/107] Compiling RefsCore RefsRename.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {
[93/107] Compiling RefsCore RefsScan.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {
[94/167] Emitting module refs_rank
[95/167] Compiling refs_rank main.swift
[95/167] Write Objects.LinkFileList
[96/167] Linking refs-rank
[97/167] Applying refs-rank
[99/167] Compiling BobMacCaptureInstallHelper BobMacCaptureInstallHelperMain.swift
[100/167] Emitting module BobMacCaptureInstallHelper
[101/167] Compiling BobMacCaptureInstallHelper InstallHelperError.swift
[102/167] Compiling BobMacCaptureInstallHelper InstallRelauncher.swift
[103/167] Compiling BobMacCaptureInstallHelper InstallHelperArguments.swift
[103/167] Write Objects.LinkFileList
[104/167] Linking BobMacCaptureInstallHelper
[105/167] Applying BobMacCaptureInstallHelper
[107/167] Emitting module BobMacCapture
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
811 |         }
812 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
811 |         }
812 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:149:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
147 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
148 |         }
149 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
150 |     }
151 | 

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[108/175] Compiling BobMacCapture AccessibilityTrust.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
811 |         }
812 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
811 |         }
812 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:76:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |         NSApplication.shared.addSceneRepresentation(representation)
 75 |         settingsSceneRepresentation = representation
 76 |         settingsPresentation = SettingsPresentation {
    |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |             representation.environment.openSettings()
 78 |         }
    :
805 |     var activateApplication: () -> Void
806 | 
807 |     init(
    |     `- note: 'init(openSettings:activateApplication:)' declared here
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:269:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
267 |         menu.addItem(redo)
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
271 |         menu.addItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:270:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
271 |         menu.addItem(
272 |             NSMenuItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:278:62: warning: use '#selector' instead of explicitly constructing a 'Selector'
276 |             )
277 |         )
278 |         menu.addItem(NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                                              `- warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |         return menu
280 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:472:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
470 |     /// off MainActor state.
471 |     nonisolated static func storedHighlightsAppPath() -> String {
472 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |     }
474 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:542:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
540 |             library: library,
541 |             opener: WorkspaceRefsOpener(),
542 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
543 |             tabs: tabsSession,
544 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:717:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
715 |             return
716 |         }
717 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
718 |     }
719 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[109/175] Compiling BobMacCapture AppDelegate.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
811 |         }
812 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
811 |         }
812 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:76:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |         NSApplication.shared.addSceneRepresentation(representation)
 75 |         settingsSceneRepresentation = representation
 76 |         settingsPresentation = SettingsPresentation {
    |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |             representation.environment.openSettings()
 78 |         }
    :
805 |     var activateApplication: () -> Void
806 | 
807 |     init(
    |     `- note: 'init(openSettings:activateApplication:)' declared here
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:269:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
267 |         menu.addItem(redo)
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
271 |         menu.addItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:270:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
271 |         menu.addItem(
272 |             NSMenuItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:278:62: warning: use '#selector' instead of explicitly constructing a 'Selector'
276 |             )
277 |         )
278 |         menu.addItem(NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                                              `- warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |         return menu
280 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:472:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
470 |     /// off MainActor state.
471 |     nonisolated static func storedHighlightsAppPath() -> String {
472 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |     }
474 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:542:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
540 |             library: library,
541 |             opener: WorkspaceRefsOpener(),
542 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
543 |             tabs: tabsSession,
544 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:717:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
715 |             return
716 |         }
717 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
718 |     }
719 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[110/175] Compiling BobMacCapture AppRelauncher.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
811 |         }
812 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
811 |         }
812 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:76:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |         NSApplication.shared.addSceneRepresentation(representation)
 75 |         settingsSceneRepresentation = representation
 76 |         settingsPresentation = SettingsPresentation {
    |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |             representation.environment.openSettings()
 78 |         }
    :
805 |     var activateApplication: () -> Void
806 | 
807 |     init(
    |     `- note: 'init(openSettings:activateApplication:)' declared here
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:269:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
267 |         menu.addItem(redo)
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
271 |         menu.addItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:270:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
271 |         menu.addItem(
272 |             NSMenuItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:278:62: warning: use '#selector' instead of explicitly constructing a 'Selector'
276 |             )
277 |         )
278 |         menu.addItem(NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                                              `- warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |         return menu
280 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:472:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
470 |     /// off MainActor state.
471 |     nonisolated static func storedHighlightsAppPath() -> String {
472 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |     }
474 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:542:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
540 |             library: library,
541 |             opener: WorkspaceRefsOpener(),
542 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
543 |             tabs: tabsSession,
544 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:717:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
715 |             return
716 |         }
717 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
718 |     }
719 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[111/175] Compiling BobMacCapture AppSettings.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
811 |         }
812 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
811 |         }
812 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:76:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |         NSApplication.shared.addSceneRepresentation(representation)
 75 |         settingsSceneRepresentation = representation
 76 |         settingsPresentation = SettingsPresentation {
    |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |             representation.environment.openSettings()
 78 |         }
    :
805 |     var activateApplication: () -> Void
806 | 
807 |     init(
    |     `- note: 'init(openSettings:activateApplication:)' declared here
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:269:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
267 |         menu.addItem(redo)
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
271 |         menu.addItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:270:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
271 |         menu.addItem(
272 |             NSMenuItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:278:62: warning: use '#selector' instead of explicitly constructing a 'Selector'
276 |             )
277 |         )
278 |         menu.addItem(NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                                              `- warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |         return menu
280 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:472:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
470 |     /// off MainActor state.
471 |     nonisolated static func storedHighlightsAppPath() -> String {
472 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |     }
474 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:542:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
540 |             library: library,
541 |             opener: WorkspaceRefsOpener(),
542 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
543 |             tabs: tabsSession,
544 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:717:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
715 |             return
716 |         }
717 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
718 |     }
719 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[112/175] Compiling BobMacCapture BlockDiffCard.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
811 |         }
812 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
811 |         }
812 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:76:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |         NSApplication.shared.addSceneRepresentation(representation)
 75 |         settingsSceneRepresentation = representation
 76 |         settingsPresentation = SettingsPresentation {
    |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |             representation.environment.openSettings()
 78 |         }
    :
805 |     var activateApplication: () -> Void
806 | 
807 |     init(
    |     `- note: 'init(openSettings:activateApplication:)' declared here
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:269:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
267 |         menu.addItem(redo)
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
271 |         menu.addItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:270:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
271 |         menu.addItem(
272 |             NSMenuItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:278:62: warning: use '#selector' instead of explicitly constructing a 'Selector'
276 |             )
277 |         )
278 |         menu.addItem(NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                                              `- warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |         return menu
280 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:472:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
470 |     /// off MainActor state.
471 |     nonisolated static func storedHighlightsAppPath() -> String {
472 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |     }
474 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:542:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
540 |             library: library,
541 |             opener: WorkspaceRefsOpener(),
542 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
543 |             tabs: tabsSession,
544 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:717:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
715 |             return
716 |         }
717 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
718 |     }
719 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[113/175] Compiling BobMacCapture BlockIDField.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
811 |         }
812 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
811 |         }
812 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:76:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |         NSApplication.shared.addSceneRepresentation(representation)
 75 |         settingsSceneRepresentation = representation
 76 |         settingsPresentation = SettingsPresentation {
    |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |             representation.environment.openSettings()
 78 |         }
    :
805 |     var activateApplication: () -> Void
806 | 
807 |     init(
    |     `- note: 'init(openSettings:activateApplication:)' declared here
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:269:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
267 |         menu.addItem(redo)
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
271 |         menu.addItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:270:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
271 |         menu.addItem(
272 |             NSMenuItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:278:62: warning: use '#selector' instead of explicitly constructing a 'Selector'
276 |             )
277 |         )
278 |         menu.addItem(NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                                              `- warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |         return menu
280 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:472:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
470 |     /// off MainActor state.
471 |     nonisolated static func storedHighlightsAppPath() -> String {
472 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |     }
474 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:542:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
540 |             library: library,
541 |             opener: WorkspaceRefsOpener(),
542 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
543 |             tabs: tabsSession,
544 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:717:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
715 |             return
716 |         }
717 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
718 |     }
719 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[114/175] Compiling BobMacCapture BobMacCaptureMain.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
811 |         }
812 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
811 |         }
812 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:76:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |         NSApplication.shared.addSceneRepresentation(representation)
 75 |         settingsSceneRepresentation = representation
 76 |         settingsPresentation = SettingsPresentation {
    |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |             representation.environment.openSettings()
 78 |         }
    :
805 |     var activateApplication: () -> Void
806 | 
807 |     init(
    |     `- note: 'init(openSettings:activateApplication:)' declared here
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:269:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
267 |         menu.addItem(redo)
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
271 |         menu.addItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:270:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
271 |         menu.addItem(
272 |             NSMenuItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:278:62: warning: use '#selector' instead of explicitly constructing a 'Selector'
276 |             )
277 |         )
278 |         menu.addItem(NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                                              `- warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |         return menu
280 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:472:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
470 |     /// off MainActor state.
471 |     nonisolated static func storedHighlightsAppPath() -> String {
472 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |     }
474 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:542:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
540 |             library: library,
541 |             opener: WorkspaceRefsOpener(),
542 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
543 |             tabs: tabsSession,
544 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:717:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
715 |             return
716 |         }
717 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
718 |     }
719 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[115/175] Compiling BobMacCapture BobPanelCoordinator.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
811 |         }
812 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
811 |         }
812 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:76:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |         NSApplication.shared.addSceneRepresentation(representation)
 75 |         settingsSceneRepresentation = representation
 76 |         settingsPresentation = SettingsPresentation {
    |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |             representation.environment.openSettings()
 78 |         }
    :
805 |     var activateApplication: () -> Void
806 | 
807 |     init(
    |     `- note: 'init(openSettings:activateApplication:)' declared here
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:269:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
267 |         menu.addItem(redo)
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
271 |         menu.addItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:270:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
271 |         menu.addItem(
272 |             NSMenuItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:278:62: warning: use '#selector' instead of explicitly constructing a 'Selector'
276 |             )
277 |         )
278 |         menu.addItem(NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                                              `- warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |         return menu
280 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:472:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
470 |     /// off MainActor state.
471 |     nonisolated static func storedHighlightsAppPath() -> String {
472 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |     }
474 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:542:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
540 |             library: library,
541 |             opener: WorkspaceRefsOpener(),
542 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
543 |             tabs: tabsSession,
544 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:717:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
715 |             return
716 |         }
717 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
718 |     }
719 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[116/175] Compiling BobMacCapture BundleSigningInspector.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
811 |         }
812 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:810:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {
810 |             NSApplication.shared.activate()
    |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
811 |         }
812 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:76:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |         NSApplication.shared.addSceneRepresentation(representation)
 75 |         settingsSceneRepresentation = representation
 76 |         settingsPresentation = SettingsPresentation {
    |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |             representation.environment.openSettings()
 78 |         }
    :
805 |     var activateApplication: () -> Void
806 | 
807 |     init(
    |     `- note: 'init(openSettings:activateApplication:)' declared here
808 |         openSettings: @escaping () -> Void = {},
809 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:269:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
267 |         menu.addItem(redo)
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
271 |         menu.addItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:270:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
268 |         menu.addItem(.separator())
269 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
270 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
271 |         menu.addItem(
272 |             NSMenuItem(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:278:62: warning: use '#selector' instead of explicitly constructing a 'Selector'
276 |             )
277 |         )
278 |         menu.addItem(NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                                              `- warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |         return menu
280 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:472:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
470 |     /// off MainActor state.
471 |     nonisolated static func storedHighlightsAppPath() -> String {
472 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |     }
474 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:542:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
540 |             library: library,
541 |             opener: WorkspaceRefsOpener(),
542 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
543 |             tabs: tabsSession,
544 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppDelegate.swift:717:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
715 |             return
716 |         }
717 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
718 |     }
719 | 

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[117/175] Compiling BobMacCapture RefsHotkeyRegistration.swift
[118/175] Compiling BobMacCapture SavedTemplateShelf.swift
[119/175] Compiling BobMacCapture SettingsView.swift
[120/175] Compiling BobMacCapture Signposts.swift
[121/175] Compiling BobMacCapture StatusItemController.swift
[122/175] Compiling BobMacCapture StatusItemGlyph.swift
[123/175] Compiling BobMacCapture TaskBlockView.swift
[124/175] Compiling BobMacCapture VaultTargetWatcher.swift
[125/175] Compiling BobMacCapture PomodoroNameField.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:149:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
147 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
148 |         }
149 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
150 |     }
151 | 
[126/175] Compiling BobMacCapture AXHighlightsTabsReader.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:149:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
147 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
148 |         }
149 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
150 |     }
151 | 
[127/175] Compiling BobMacCapture RefsActionsMenu.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:149:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
147 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
148 |         }
149 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
150 |     }
151 | 
[128/175] Compiling BobMacCapture RefsCopyCardView.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:149:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
147 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
148 |         }
149 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
150 |     }
151 | 
[129/175] Compiling BobMacCapture RefsCopyHUD.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:149:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
147 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
148 |         }
149 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
150 |     }
151 | 
[130/175] Compiling BobMacCapture RefsFooter.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:149:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
147 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
148 |         }
149 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
150 |     }
151 | 
[131/175] Compiling BobMacCapture RefsInspectorLoader.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:149:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
147 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
148 |         }
149 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
150 |     }
151 | 
[132/175] Compiling BobMacCapture RefsInspectorScroll.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:149:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
147 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
148 |         }
149 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
150 |     }
151 | 
[133/175] Compiling BobMacCapture CapturePullInChoiceView.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[134/175] Compiling BobMacCapture CaptureSnippetResolver.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[135/175] Compiling BobMacCapture HighlightsTakeover.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[136/175] Compiling BobMacCapture HotKeyRegistry.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[137/175] Compiling BobMacCapture NotificationService.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[138/175] Compiling BobMacCapture PlainTextPaste.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[139/175] Compiling BobMacCapture PomodoroBlockView.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[140/175] Compiling BobMacCapture PomodoroHomeColor.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[141/175] Compiling BobMacCapture CanceledDraftStash.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[142/175] Compiling BobMacCapture CaptureAgendaRowMeasurer.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[143/175] Compiling BobMacCapture CaptureAgendaStore.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[144/175] Compiling BobMacCapture CaptureAgendaView.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[145/175] Compiling BobMacCapture CaptureEditorPalette.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[146/175] Compiling BobMacCapture CaptureEditorTextConfiguration.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[147/175] Compiling BobMacCapture CaptureKeyCommandRouter.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[148/175] Compiling BobMacCapture CapturePanelController.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[149/175] Compiling BobMacCapture RefsInspectorView.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:476:27: warning: expression of type 'Bool' is unused [#no-usage]
474 |     private func refreshSnapshotAfterRename() async {
475 |         while let current = snapshotTask {
476 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
477 |         }
478 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:480:27: warning: expression of type 'Bool' is unused [#no-usage]
478 |         refreshSnapshot(reason: .manual)
479 |         while let current = snapshotTask {
480 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
481 |         }
482 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:737:27: warning: expression of type 'Bool' is unused [#no-usage]
735 |     private func runPostScanRefresh() async {
736 |         while let current = snapshotTask {
737 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
738 |             if snapshotTask == nil {
739 |                 break

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:744:27: warning: expression of type 'Bool' is unused [#no-usage]
742 |         refresh(reason: .scan)
743 |         while let current = snapshotTask {
744 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
745 |             if snapshotTask == nil {
746 |                 break

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:806:24: warning: no 'async' operations occur within 'await' expression
804 |                     return
805 |                 }
806 |                 Task { await self?.handleWatcherChange() }
    |                        `- warning: no 'async' operations occur within 'await' expression
807 |             },
808 |             onFailure: { [weak self] message in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:809:24: warning: no 'async' operations occur within 'await' expression
807 |             },
808 |             onFailure: { [weak self] message in
809 |                 Task { await self?.watcherFailed(message) }
    |                        `- warning: no 'async' operations occur within 'await' expression
810 |             }
811 |         )

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsListView.swift:189:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
187 |                 // rows report nil, which never clears the current rect.
188 |                 .onGeometryChange(for: CGRect?.self) { proxy in
189 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
190 |                         ? proxy.frame(in: .named("refsPanel")) : nil
191 |                 } action: { rect in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:287:40: note: property declared here
 285 |         return tabsFilter && tabsListing?.tabs[id] != nil
 286 |     }
 287 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 288 |         didSet {
 289 |             if oldValue != selectedID {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsListView.swift:227:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
225 |             .transition(removalTransition)
226 |             .onGeometryChange(for: CGRect?.self) { proxy in
227 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
228 |                     ? proxy.frame(in: .named("refsPanel")) : nil
229 |             } action: { rect in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:287:40: note: property declared here
 285 |         return tabsFilter && tabsListing?.tabs[id] != nil
 286 |     }
 287 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 288 |         didSet {
 289 |             if oldValue != selectedID {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:181:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 179 |         completion: @escaping (Error?) -> Void
 180 |     ) {
 181 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 182 |         configuration.activates = true
 183 |         NSWorkspace.shared.open(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:204:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 202 | 
 203 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 204 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 205 |         configuration.activates = true
 206 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:554:20: warning: no 'async' operations occur within 'await' expression
 552 |         }.store(in: &subscriptions)
 553 |         let itemsSubscription = library.$items.sink { [weak self] _ in
 554 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 555 |         }
 556 |         let signalsSubscription = library.$signals.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:557:20: warning: no 'async' operations occur within 'await' expression
 555 |         }
 556 |         let signalsSubscription = library.$signals.sink { [weak self] _ in
 557 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 558 |         }
 559 |         itemsSubscription.store(in: &subscriptions)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:562:20: warning: no 'async' operations occur within 'await' expression
 560 |         signalsSubscription.store(in: &subscriptions)
 561 |         library.$todayRefreshGeneration.sink { [weak self] _ in
 562 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 563 |         }.store(in: &subscriptions)
 564 |         library.$scanState.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:565:20: warning: no 'async' operations occur within 'await' expression
 563 |         }.store(in: &subscriptions)
 564 |         library.$scanState.sink { [weak self] _ in
 565 |             Task { await self?.scanStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 566 |         }.store(in: &subscriptions)
 567 |         library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:568:20: warning: no 'async' operations occur within 'await' expression
 566 |         }.store(in: &subscriptions)
 567 |         library.$refreshState.sink { [weak self] _ in
 568 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 569 |         }.store(in: &subscriptions)
 570 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2648:13: warning: result of call to 'openSelected' is unused [#no-usage]
2646 |             openWithDefaultApp(item)
2647 |         case .note, .reveal:
2648 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
2649 |         }
2650 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2680:17: warning: no 'async' operations occur within 'await' expression
2678 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
2679 |             Task {
2680 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
2681 |             }
2682 |         }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2707:17: warning: no 'async' operations occur within 'await' expression
2705 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
2706 |             Task {
2707 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
2708 |             }
2709 |         }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2765:17: warning: no 'async' operations occur within 'await' expression
2763 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
2764 |             Task {
2765 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
2766 |                     itemID: item.id,
2767 |                     title: item.title.text,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2796:17: warning: no 'async' operations occur within 'await' expression
2794 |         opener.openWithDefaultApp(pdf) { [weak self] error in
2795 |             Task {
2796 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
2797 |                     itemID: item.id,
2798 |                     title: item.title.text,
[150/175] Compiling BobMacCapture RefsKeyRouter.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:476:27: warning: expression of type 'Bool' is unused [#no-usage]
474 |     private func refreshSnapshotAfterRename() async {
475 |         while let current = snapshotTask {
476 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
477 |         }
478 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:480:27: warning: expression of type 'Bool' is unused [#no-usage]
478 |         refreshSnapshot(reason: .manual)
479 |         while let current = snapshotTask {
480 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
481 |         }
482 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:737:27: warning: expression of type 'Bool' is unused [#no-usage]
735 |     private func runPostScanRefresh() async {
736 |         while let current = snapshotTask {
737 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
738 |             if snapshotTask == nil {
739 |                 break

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:744:27: warning: expression of type 'Bool' is unused [#no-usage]
742 |         refresh(reason: .scan)
743 |         while let current = snapshotTask {
744 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
745 |             if snapshotTask == nil {
746 |                 break

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:806:24: warning: no 'async' operations occur within 'await' expression
804 |                     return
805 |                 }
806 |                 Task { await self?.handleWatcherChange() }
    |                        `- warning: no 'async' operations occur within 'await' expression
807 |             },
808 |             onFailure: { [weak self] message in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:809:24: warning: no 'async' operations occur within 'await' expression
807 |             },
808 |             onFailure: { [weak self] message in
809 |                 Task { await self?.watcherFailed(message) }
    |                        `- warning: no 'async' operations occur within 'await' expression
810 |             }
811 |         )

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsListView.swift:189:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
187 |                 // rows report nil, which never clears the current rect.
188 |                 .onGeometryChange(for: CGRect?.self) { proxy in
189 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
190 |                         ? proxy.frame(in: .named("refsPanel")) : nil
191 |                 } action: { rect in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:287:40: note: property declared here
 285 |         return tabsFilter && tabsListing?.tabs[id] != nil
 286 |     }
 287 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 288 |         didSet {
 289 |             if oldValue != selectedID {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsListView.swift:227:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
225 |             .transition(removalTransition)
226 |             .onGeometryChange(for: CGRect?.self) { proxy in
227 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
228 |                     ? proxy.frame(in: .named("refsPanel")) : nil
229 |             } action: { rect in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:287:40: note: property declared here
 285 |         return tabsFilter && tabsListing?.tabs[id] != nil
 286 |     }
 287 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 288 |         didSet {
 289 |             if oldValue != selectedID {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:181:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 179 |         completion: @escaping (Error?) -> Void
 180 |     ) {
 181 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 182 |         configuration.activates = true
 183 |         NSWorkspace.shared.open(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:204:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 202 | 
 203 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 204 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 205 |         configuration.activates = true
 206 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:554:20: warning: no 'async' operations occur within 'await' expression
 552 |         }.store(in: &subscriptions)
 553 |         let itemsSubscription = library.$items.sink { [weak self] _ in
 554 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 555 |         }
 556 |         let signalsSubscription = library.$signals.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:557:20: warning: no 'async' operations occur within 'await' expression
 555 |         }
 556 |         let signalsSubscription = library.$signals.sink { [weak self] _ in
 557 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 558 |         }
 559 |         itemsSubscription.store(in: &subscriptions)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:562:20: warning: no 'async' operations occur within 'await' expression
 560 |         signalsSubscription.store(in: &subscriptions)
 561 |         library.$todayRefreshGeneration.sink { [weak self] _ in
 562 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 563 |         }.store(in: &subscriptions)
 564 |         library.$scanState.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:565:20: warning: no 'async' operations occur within 'await' expression
 563 |         }.store(in: &subscriptions)
 564 |         library.$scanState.sink { [weak self] _ in
 565 |             Task { await self?.scanStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 566 |         }.store(in: &subscriptions)
 567 |         library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:568:20: warning: no 'async' operations occur within 'await' expression
 566 |         }.store(in: &subscriptions)
 567 |         library.$refreshState.sink { [weak self] _ in
 568 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 569 |         }.store(in: &subscriptions)
 570 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2648:13: warning: result of call to 'openSelected' is unused [#no-usage]
2646 |             openWithDefaultApp(item)
2647 |         case .note, .reveal:
2648 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
2649 |         }
2650 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2680:17: warning: no 'async' operations occur within 'await' expression
2678 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
2679 |             Task {
2680 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
2681 |             }
2682 |         }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2707:17: warning: no 'async' operations occur within 'await' expression
2705 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
2706 |             Task {
2707 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
2708 |             }
2709 |         }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2765:17: warning: no 'async' operations occur within 'await' expression
2763 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
2764 |             Task {
2765 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
2766 |                     itemID: item.id,
2767 |                     title: item.title.text,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2796:17: warning: no 'async' operations occur within 'await' expression
2794 |         opener.openWithDefaultApp(pdf) { [weak self] error in
2795 |             Task {
2796 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
2797 |                     itemID: item.id,
2798 |                     title: item.title.text,
[151/175] Compiling BobMacCapture RefsLibrary.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:476:27: warning: expression of type 'Bool' is unused [#no-usage]
474 |     private func refreshSnapshotAfterRename() async {
475 |         while let current = snapshotTask {
476 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
477 |         }
478 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:480:27: warning: expression of type 'Bool' is unused [#no-usage]
478 |         refreshSnapshot(reason: .manual)
479 |         while let current = snapshotTask {
480 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
481 |         }
482 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:737:27: warning: expression of type 'Bool' is unused [#no-usage]
735 |     private func runPostScanRefresh() async {
736 |         while let current = snapshotTask {
737 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
738 |             if snapshotTask == nil {
739 |                 break

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:744:27: warning: expression of type 'Bool' is unused [#no-usage]
742 |         refresh(reason: .scan)
743 |         while let current = snapshotTask {
744 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
745 |             if snapshotTask == nil {
746 |                 break

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:806:24: warning: no 'async' operations occur within 'await' expression
804 |                     return
805 |                 }
806 |                 Task { await self?.handleWatcherChange() }
    |                        `- warning: no 'async' operations occur within 'await' expression
807 |             },
808 |             onFailure: { [weak self] message in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:809:24: warning: no 'async' operations occur within 'await' expression
807 |             },
808 |             onFailure: { [weak self] message in
809 |                 Task { await self?.watcherFailed(message) }
    |                        `- warning: no 'async' operations occur within 'await' expression
810 |             }
811 |         )

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsListView.swift:189:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
187 |                 // rows report nil, which never clears the current rect.
188 |                 .onGeometryChange(for: CGRect?.self) { proxy in
189 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
190 |                         ? proxy.frame(in: .named("refsPanel")) : nil
191 |                 } action: { rect in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:287:40: note: property declared here
 285 |         return tabsFilter && tabsListing?.tabs[id] != nil
 286 |     }
 287 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 288 |         didSet {
 289 |             if oldValue != selectedID {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsListView.swift:227:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
225 |             .transition(removalTransition)
226 |             .onGeometryChange(for: CGRect?.self) { proxy in
227 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
228 |                     ? proxy.frame(in: .named("refsPanel")) : nil
229 |             } action: { rect in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:287:40: note: property declared here
 285 |         return tabsFilter && tabsListing?.tabs[id] != nil
 286 |     }
 287 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 288 |         didSet {
 289 |             if oldValue != selectedID {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:181:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 179 |         completion: @escaping (Error?) -> Void
 180 |     ) {
 181 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 182 |         configuration.activates = true
 183 |         NSWorkspace.shared.open(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:204:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 202 | 
 203 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 204 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 205 |         configuration.activates = true
 206 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:554:20: warning: no 'async' operations occur within 'await' expression
 552 |         }.store(in: &subscriptions)
 553 |         let itemsSubscription = library.$items.sink { [weak self] _ in
 554 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 555 |         }
 556 |         let signalsSubscription = library.$signals.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:557:20: warning: no 'async' operations occur within 'await' expression
 555 |         }
 556 |         let signalsSubscription = library.$signals.sink { [weak self] _ in
 557 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 558 |         }
 559 |         itemsSubscription.store(in: &subscriptions)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:562:20: warning: no 'async' operations occur within 'await' expression
 560 |         signalsSubscription.store(in: &subscriptions)
 561 |         library.$todayRefreshGeneration.sink { [weak self] _ in
 562 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 563 |         }.store(in: &subscriptions)
 564 |         library.$scanState.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:565:20: warning: no 'async' operations occur within 'await' expression
 563 |         }.store(in: &subscriptions)
 564 |         library.$scanState.sink { [weak self] _ in
 565 |             Task { await self?.scanStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 566 |         }.store(in: &subscriptions)
 567 |         library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:568:20: warning: no 'async' operations occur within 'await' expression
 566 |         }.store(in: &subscriptions)
 567 |         library.$refreshState.sink { [weak self] _ in
 568 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 569 |         }.store(in: &subscriptions)
 570 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2648:13: warning: result of call to 'openSelected' is unused [#no-usage]
2646 |             openWithDefaultApp(item)
2647 |         case .note, .reveal:
2648 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
2649 |         }
2650 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2680:17: warning: no 'async' operations occur within 'await' expression
2678 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
2679 |             Task {
2680 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
2681 |             }
2682 |         }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2707:17: warning: no 'async' operations occur within 'await' expression
2705 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
2706 |             Task {
2707 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
2708 |             }
2709 |         }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2765:17: warning: no 'async' operations occur within 'await' expression
2763 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
2764 |             Task {
2765 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
2766 |                     itemID: item.id,
2767 |                     title: item.title.text,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2796:17: warning: no 'async' operations occur within 'await' expression
2794 |         opener.openWithDefaultApp(pdf) { [weak self] error in
2795 |             Task {
2796 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
2797 |                     itemID: item.id,
2798 |                     title: item.title.text,
[152/175] Compiling BobMacCapture RefsListView.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:476:27: warning: expression of type 'Bool' is unused [#no-usage]
474 |     private func refreshSnapshotAfterRename() async {
475 |         while let current = snapshotTask {
476 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
477 |         }
478 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:480:27: warning: expression of type 'Bool' is unused [#no-usage]
478 |         refreshSnapshot(reason: .manual)
479 |         while let current = snapshotTask {
480 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
481 |         }
482 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:737:27: warning: expression of type 'Bool' is unused [#no-usage]
735 |     private func runPostScanRefresh() async {
736 |         while let current = snapshotTask {
737 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
738 |             if snapshotTask == nil {
739 |                 break

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:744:27: warning: expression of type 'Bool' is unused [#no-usage]
742 |         refresh(reason: .scan)
743 |         while let current = snapshotTask {
744 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
745 |             if snapshotTask == nil {
746 |                 break

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:806:24: warning: no 'async' operations occur within 'await' expression
804 |                     return
805 |                 }
806 |                 Task { await self?.handleWatcherChange() }
    |                        `- warning: no 'async' operations occur within 'await' expression
807 |             },
808 |             onFailure: { [weak self] message in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:809:24: warning: no 'async' operations occur within 'await' expression
807 |             },
808 |             onFailure: { [weak self] message in
809 |                 Task { await self?.watcherFailed(message) }
    |                        `- warning: no 'async' operations occur within 'await' expression
810 |             }
811 |         )

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsListView.swift:189:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
187 |                 // rows report nil, which never clears the current rect.
188 |                 .onGeometryChange(for: CGRect?.self) { proxy in
189 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
190 |                         ? proxy.frame(in: .named("refsPanel")) : nil
191 |                 } action: { rect in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:287:40: note: property declared here
 285 |         return tabsFilter && tabsListing?.tabs[id] != nil
 286 |     }
 287 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 288 |         didSet {
 289 |             if oldValue != selectedID {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsListView.swift:227:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
225 |             .transition(removalTransition)
226 |             .onGeometryChange(for: CGRect?.self) { proxy in
227 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
228 |                     ? proxy.frame(in: .named("refsPanel")) : nil
229 |             } action: { rect in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:287:40: note: property declared here
 285 |         return tabsFilter && tabsListing?.tabs[id] != nil
 286 |     }
 287 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 288 |         didSet {
 289 |             if oldValue != selectedID {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:181:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 179 |         completion: @escaping (Error?) -> Void
 180 |     ) {
 181 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 182 |         configuration.activates = true
 183 |         NSWorkspace.shared.open(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:204:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 202 | 
 203 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 204 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 205 |         configuration.activates = true
 206 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:554:20: warning: no 'async' operations occur within 'await' expression
 552 |         }.store(in: &subscriptions)
 553 |         let itemsSubscription = library.$items.sink { [weak self] _ in
 554 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 555 |         }
 556 |         let signalsSubscription = library.$signals.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:557:20: warning: no 'async' operations occur within 'await' expression
 555 |         }
 556 |         let signalsSubscription = library.$signals.sink { [weak self] _ in
 557 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 558 |         }
 559 |         itemsSubscription.store(in: &subscriptions)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:562:20: warning: no 'async' operations occur within 'await' expression
 560 |         signalsSubscription.store(in: &subscriptions)
 561 |         library.$todayRefreshGeneration.sink { [weak self] _ in
 562 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 563 |         }.store(in: &subscriptions)
 564 |         library.$scanState.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:565:20: warning: no 'async' operations occur within 'await' expression
 563 |         }.store(in: &subscriptions)
 564 |         library.$scanState.sink { [weak self] _ in
 565 |             Task { await self?.scanStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 566 |         }.store(in: &subscriptions)
 567 |         library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:568:20: warning: no 'async' operations occur within 'await' expression
 566 |         }.store(in: &subscriptions)
 567 |         library.$refreshState.sink { [weak self] _ in
 568 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 569 |         }.store(in: &subscriptions)
 570 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2648:13: warning: result of call to 'openSelected' is unused [#no-usage]
2646 |             openWithDefaultApp(item)
2647 |         case .note, .reveal:
2648 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
2649 |         }
2650 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2680:17: warning: no 'async' operations occur within 'await' expression
2678 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
2679 |             Task {
2680 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
2681 |             }
2682 |         }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2707:17: warning: no 'async' operations occur within 'await' expression
2705 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
2706 |             Task {
2707 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
2708 |             }
2709 |         }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2765:17: warning: no 'async' operations occur within 'await' expression
2763 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
2764 |             Task {
2765 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
2766 |                     itemID: item.id,
2767 |                     title: item.title.text,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2796:17: warning: no 'async' operations occur within 'await' expression
2794 |         opener.openWithDefaultApp(pdf) { [weak self] error in
2795 |             Task {
2796 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
2797 |                     itemID: item.id,
2798 |                     title: item.title.text,
[153/175] Compiling BobMacCapture RefsPanel.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:476:27: warning: expression of type 'Bool' is unused [#no-usage]
474 |     private func refreshSnapshotAfterRename() async {
475 |         while let current = snapshotTask {
476 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
477 |         }
478 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:480:27: warning: expression of type 'Bool' is unused [#no-usage]
478 |         refreshSnapshot(reason: .manual)
479 |         while let current = snapshotTask {
480 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
481 |         }
482 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:737:27: warning: expression of type 'Bool' is unused [#no-usage]
735 |     private func runPostScanRefresh() async {
736 |         while let current = snapshotTask {
737 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
738 |             if snapshotTask == nil {
739 |                 break

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:744:27: warning: expression of type 'Bool' is unused [#no-usage]
742 |         refresh(reason: .scan)
743 |         while let current = snapshotTask {
744 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
745 |             if snapshotTask == nil {
746 |                 break

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:806:24: warning: no 'async' operations occur within 'await' expression
804 |                     return
805 |                 }
806 |                 Task { await self?.handleWatcherChange() }
    |                        `- warning: no 'async' operations occur within 'await' expression
807 |             },
808 |             onFailure: { [weak self] message in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:809:24: warning: no 'async' operations occur within 'await' expression
807 |             },
808 |             onFailure: { [weak self] message in
809 |                 Task { await self?.watcherFailed(message) }
    |                        `- warning: no 'async' operations occur within 'await' expression
810 |             }
811 |         )

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsListView.swift:189:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
187 |                 // rows report nil, which never clears the current rect.
188 |                 .onGeometryChange(for: CGRect?.self) { proxy in
189 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
190 |                         ? proxy.frame(in: .named("refsPanel")) : nil
191 |                 } action: { rect in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:287:40: note: property declared here
 285 |         return tabsFilter && tabsListing?.tabs[id] != nil
 286 |     }
 287 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 288 |         didSet {
 289 |             if oldValue != selectedID {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsListView.swift:227:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
225 |             .transition(removalTransition)
226 |             .onGeometryChange(for: CGRect?.self) { proxy in
227 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
228 |                     ? proxy.frame(in: .named("refsPanel")) : nil
229 |             } action: { rect in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:287:40: note: property declared here
 285 |         return tabsFilter && tabsListing?.tabs[id] != nil
 286 |     }
 287 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 288 |         didSet {
 289 |             if oldValue != selectedID {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:181:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 179 |         completion: @escaping (Error?) -> Void
 180 |     ) {
 181 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 182 |         configuration.activates = true
 183 |         NSWorkspace.shared.open(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:204:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 202 | 
 203 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 204 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 205 |         configuration.activates = true
 206 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:554:20: warning: no 'async' operations occur within 'await' expression
 552 |         }.store(in: &subscriptions)
 553 |         let itemsSubscription = library.$items.sink { [weak self] _ in
 554 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 555 |         }
 556 |         let signalsSubscription = library.$signals.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:557:20: warning: no 'async' operations occur within 'await' expression
 555 |         }
 556 |         let signalsSubscription = library.$signals.sink { [weak self] _ in
 557 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 558 |         }
 559 |         itemsSubscription.store(in: &subscriptions)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:562:20: warning: no 'async' operations occur within 'await' expression
 560 |         signalsSubscription.store(in: &subscriptions)
 561 |         library.$todayRefreshGeneration.sink { [weak self] _ in
 562 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 563 |         }.store(in: &subscriptions)
 564 |         library.$scanState.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:565:20: warning: no 'async' operations occur within 'await' expression
 563 |         }.store(in: &subscriptions)
 564 |         library.$scanState.sink { [weak self] _ in
 565 |             Task { await self?.scanStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 566 |         }.store(in: &subscriptions)
 567 |         library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:568:20: warning: no 'async' operations occur within 'await' expression
 566 |         }.store(in: &subscriptions)
 567 |         library.$refreshState.sink { [weak self] _ in
 568 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 569 |         }.store(in: &subscriptions)
 570 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2648:13: warning: result of call to 'openSelected' is unused [#no-usage]
2646 |             openWithDefaultApp(item)
2647 |         case .note, .reveal:
2648 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
2649 |         }
2650 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2680:17: warning: no 'async' operations occur within 'await' expression
2678 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
2679 |             Task {
2680 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
2681 |             }
2682 |         }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2707:17: warning: no 'async' operations occur within 'await' expression
2705 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
2706 |             Task {
2707 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
2708 |             }
2709 |         }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2765:17: warning: no 'async' operations occur within 'await' expression
2763 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
2764 |             Task {
2765 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
2766 |                     itemID: item.id,
2767 |                     title: item.title.text,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2796:17: warning: no 'async' operations occur within 'await' expression
2794 |         opener.openWithDefaultApp(pdf) { [weak self] error in
2795 |             Task {
2796 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
2797 |                     itemID: item.id,
2798 |                     title: item.title.text,
[154/175] Compiling BobMacCapture RefsPanelModel.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:476:27: warning: expression of type 'Bool' is unused [#no-usage]
474 |     private func refreshSnapshotAfterRename() async {
475 |         while let current = snapshotTask {
476 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
477 |         }
478 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:480:27: warning: expression of type 'Bool' is unused [#no-usage]
478 |         refreshSnapshot(reason: .manual)
479 |         while let current = snapshotTask {
480 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
481 |         }
482 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:737:27: warning: expression of type 'Bool' is unused [#no-usage]
735 |     private func runPostScanRefresh() async {
736 |         while let current = snapshotTask {
737 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
738 |             if snapshotTask == nil {
739 |                 break

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:744:27: warning: expression of type 'Bool' is unused [#no-usage]
742 |         refresh(reason: .scan)
743 |         while let current = snapshotTask {
744 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
745 |             if snapshotTask == nil {
746 |                 break

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:806:24: warning: no 'async' operations occur within 'await' expression
804 |                     return
805 |                 }
806 |                 Task { await self?.handleWatcherChange() }
    |                        `- warning: no 'async' operations occur within 'await' expression
807 |             },
808 |             onFailure: { [weak self] message in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:809:24: warning: no 'async' operations occur within 'await' expression
807 |             },
808 |             onFailure: { [weak self] message in
809 |                 Task { await self?.watcherFailed(message) }
    |                        `- warning: no 'async' operations occur within 'await' expression
810 |             }
811 |         )

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsListView.swift:189:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
187 |                 // rows report nil, which never clears the current rect.
188 |                 .onGeometryChange(for: CGRect?.self) { proxy in
189 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
190 |                         ? proxy.frame(in: .named("refsPanel")) : nil
191 |                 } action: { rect in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:287:40: note: property declared here
 285 |         return tabsFilter && tabsListing?.tabs[id] != nil
 286 |     }
 287 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 288 |         didSet {
 289 |             if oldValue != selectedID {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsListView.swift:227:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
225 |             .transition(removalTransition)
226 |             .onGeometryChange(for: CGRect?.self) { proxy in
227 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
228 |                     ? proxy.frame(in: .named("refsPanel")) : nil
229 |             } action: { rect in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:287:40: note: property declared here
 285 |         return tabsFilter && tabsListing?.tabs[id] != nil
 286 |     }
 287 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 288 |         didSet {
 289 |             if oldValue != selectedID {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:181:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 179 |         completion: @escaping (Error?) -> Void
 180 |     ) {
 181 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 182 |         configuration.activates = true
 183 |         NSWorkspace.shared.open(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:204:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 202 | 
 203 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 204 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 205 |         configuration.activates = true
 206 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:554:20: warning: no 'async' operations occur within 'await' expression
 552 |         }.store(in: &subscriptions)
 553 |         let itemsSubscription = library.$items.sink { [weak self] _ in
 554 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 555 |         }
 556 |         let signalsSubscription = library.$signals.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:557:20: warning: no 'async' operations occur within 'await' expression
 555 |         }
 556 |         let signalsSubscription = library.$signals.sink { [weak self] _ in
 557 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 558 |         }
 559 |         itemsSubscription.store(in: &subscriptions)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:562:20: warning: no 'async' operations occur within 'await' expression
 560 |         signalsSubscription.store(in: &subscriptions)
 561 |         library.$todayRefreshGeneration.sink { [weak self] _ in
 562 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 563 |         }.store(in: &subscriptions)
 564 |         library.$scanState.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:565:20: warning: no 'async' operations occur within 'await' expression
 563 |         }.store(in: &subscriptions)
 564 |         library.$scanState.sink { [weak self] _ in
 565 |             Task { await self?.scanStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 566 |         }.store(in: &subscriptions)
 567 |         library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:568:20: warning: no 'async' operations occur within 'await' expression
 566 |         }.store(in: &subscriptions)
 567 |         library.$refreshState.sink { [weak self] _ in
 568 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 569 |         }.store(in: &subscriptions)
 570 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2648:13: warning: result of call to 'openSelected' is unused [#no-usage]
2646 |             openWithDefaultApp(item)
2647 |         case .note, .reveal:
2648 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
2649 |         }
2650 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2680:17: warning: no 'async' operations occur within 'await' expression
2678 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
2679 |             Task {
2680 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
2681 |             }
2682 |         }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2707:17: warning: no 'async' operations occur within 'await' expression
2705 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
2706 |             Task {
2707 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
2708 |             }
2709 |         }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2765:17: warning: no 'async' operations occur within 'await' expression
2763 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
2764 |             Task {
2765 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
2766 |                     itemID: item.id,
2767 |                     title: item.title.text,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2796:17: warning: no 'async' operations occur within 'await' expression
2794 |         opener.openWithDefaultApp(pdf) { [weak self] error in
2795 |             Task {
2796 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
2797 |                     itemID: item.id,
2798 |                     title: item.title.text,
[155/175] Compiling BobMacCapture RefsPanelStates.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:476:27: warning: expression of type 'Bool' is unused [#no-usage]
474 |     private func refreshSnapshotAfterRename() async {
475 |         while let current = snapshotTask {
476 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
477 |         }
478 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:480:27: warning: expression of type 'Bool' is unused [#no-usage]
478 |         refreshSnapshot(reason: .manual)
479 |         while let current = snapshotTask {
480 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
481 |         }
482 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:737:27: warning: expression of type 'Bool' is unused [#no-usage]
735 |     private func runPostScanRefresh() async {
736 |         while let current = snapshotTask {
737 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
738 |             if snapshotTask == nil {
739 |                 break

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:744:27: warning: expression of type 'Bool' is unused [#no-usage]
742 |         refresh(reason: .scan)
743 |         while let current = snapshotTask {
744 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
745 |             if snapshotTask == nil {
746 |                 break

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:806:24: warning: no 'async' operations occur within 'await' expression
804 |                     return
805 |                 }
806 |                 Task { await self?.handleWatcherChange() }
    |                        `- warning: no 'async' operations occur within 'await' expression
807 |             },
808 |             onFailure: { [weak self] message in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:809:24: warning: no 'async' operations occur within 'await' expression
807 |             },
808 |             onFailure: { [weak self] message in
809 |                 Task { await self?.watcherFailed(message) }
    |                        `- warning: no 'async' operations occur within 'await' expression
810 |             }
811 |         )

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsListView.swift:189:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
187 |                 // rows report nil, which never clears the current rect.
188 |                 .onGeometryChange(for: CGRect?.self) { proxy in
189 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
190 |                         ? proxy.frame(in: .named("refsPanel")) : nil
191 |                 } action: { rect in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:287:40: note: property declared here
 285 |         return tabsFilter && tabsListing?.tabs[id] != nil
 286 |     }
 287 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 288 |         didSet {
 289 |             if oldValue != selectedID {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsListView.swift:227:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
225 |             .transition(removalTransition)
226 |             .onGeometryChange(for: CGRect?.self) { proxy in
227 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
228 |                     ? proxy.frame(in: .named("refsPanel")) : nil
229 |             } action: { rect in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:287:40: note: property declared here
 285 |         return tabsFilter && tabsListing?.tabs[id] != nil
 286 |     }
 287 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 288 |         didSet {
 289 |             if oldValue != selectedID {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:181:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 179 |         completion: @escaping (Error?) -> Void
 180 |     ) {
 181 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 182 |         configuration.activates = true
 183 |         NSWorkspace.shared.open(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:204:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 202 | 
 203 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 204 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 205 |         configuration.activates = true
 206 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:554:20: warning: no 'async' operations occur within 'await' expression
 552 |         }.store(in: &subscriptions)
 553 |         let itemsSubscription = library.$items.sink { [weak self] _ in
 554 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 555 |         }
 556 |         let signalsSubscription = library.$signals.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:557:20: warning: no 'async' operations occur within 'await' expression
 555 |         }
 556 |         let signalsSubscription = library.$signals.sink { [weak self] _ in
 557 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 558 |         }
 559 |         itemsSubscription.store(in: &subscriptions)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:562:20: warning: no 'async' operations occur within 'await' expression
 560 |         signalsSubscription.store(in: &subscriptions)
 561 |         library.$todayRefreshGeneration.sink { [weak self] _ in
 562 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 563 |         }.store(in: &subscriptions)
 564 |         library.$scanState.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:565:20: warning: no 'async' operations occur within 'await' expression
 563 |         }.store(in: &subscriptions)
 564 |         library.$scanState.sink { [weak self] _ in
 565 |             Task { await self?.scanStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 566 |         }.store(in: &subscriptions)
 567 |         library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:568:20: warning: no 'async' operations occur within 'await' expression
 566 |         }.store(in: &subscriptions)
 567 |         library.$refreshState.sink { [weak self] _ in
 568 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 569 |         }.store(in: &subscriptions)
 570 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2648:13: warning: result of call to 'openSelected' is unused [#no-usage]
2646 |             openWithDefaultApp(item)
2647 |         case .note, .reveal:
2648 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
2649 |         }
2650 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2680:17: warning: no 'async' operations occur within 'await' expression
2678 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
2679 |             Task {
2680 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
2681 |             }
2682 |         }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2707:17: warning: no 'async' operations occur within 'await' expression
2705 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
2706 |             Task {
2707 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
2708 |             }
2709 |         }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2765:17: warning: no 'async' operations occur within 'await' expression
2763 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
2764 |             Task {
2765 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
2766 |                     itemID: item.id,
2767 |                     title: item.title.text,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2796:17: warning: no 'async' operations occur within 'await' expression
2794 |         opener.openWithDefaultApp(pdf) { [weak self] error in
2795 |             Task {
2796 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
2797 |                     itemID: item.id,
2798 |                     title: item.title.text,
[156/175] Compiling BobMacCapture RefsPanelView.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:476:27: warning: expression of type 'Bool' is unused [#no-usage]
474 |     private func refreshSnapshotAfterRename() async {
475 |         while let current = snapshotTask {
476 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
477 |         }
478 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:480:27: warning: expression of type 'Bool' is unused [#no-usage]
478 |         refreshSnapshot(reason: .manual)
479 |         while let current = snapshotTask {
480 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
481 |         }
482 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:737:27: warning: expression of type 'Bool' is unused [#no-usage]
735 |     private func runPostScanRefresh() async {
736 |         while let current = snapshotTask {
737 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
738 |             if snapshotTask == nil {
739 |                 break

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:744:27: warning: expression of type 'Bool' is unused [#no-usage]
742 |         refresh(reason: .scan)
743 |         while let current = snapshotTask {
744 |             await current.value
    |                           `- warning: expression of type 'Bool' is unused [#no-usage]
745 |             if snapshotTask == nil {
746 |                 break

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:806:24: warning: no 'async' operations occur within 'await' expression
804 |                     return
805 |                 }
806 |                 Task { await self?.handleWatcherChange() }
    |                        `- warning: no 'async' operations occur within 'await' expression
807 |             },
808 |             onFailure: { [weak self] message in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsLibrary.swift:809:24: warning: no 'async' operations occur within 'await' expression
807 |             },
808 |             onFailure: { [weak self] message in
809 |                 Task { await self?.watcherFailed(message) }
    |                        `- warning: no 'async' operations occur within 'await' expression
810 |             }
811 |         )

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsListView.swift:189:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
187 |                 // rows report nil, which never clears the current rect.
188 |                 .onGeometryChange(for: CGRect?.self) { proxy in
189 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
190 |                         ? proxy.frame(in: .named("refsPanel")) : nil
191 |                 } action: { rect in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:287:40: note: property declared here
 285 |         return tabsFilter && tabsListing?.tabs[id] != nil
 286 |     }
 287 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 288 |         didSet {
 289 |             if oldValue != selectedID {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsListView.swift:227:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
225 |             .transition(removalTransition)
226 |             .onGeometryChange(for: CGRect?.self) { proxy in
227 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
228 |                     ? proxy.frame(in: .named("refsPanel")) : nil
229 |             } action: { rect in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:287:40: note: property declared here
 285 |         return tabsFilter && tabsListing?.tabs[id] != nil
 286 |     }
 287 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 288 |         didSet {
 289 |             if oldValue != selectedID {

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:181:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 179 |         completion: @escaping (Error?) -> Void
 180 |     ) {
 181 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 182 |         configuration.activates = true
 183 |         NSWorkspace.shared.open(

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:204:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 202 | 
 203 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 204 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 205 |         configuration.activates = true
 206 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:554:20: warning: no 'async' operations occur within 'await' expression
 552 |         }.store(in: &subscriptions)
 553 |         let itemsSubscription = library.$items.sink { [weak self] _ in
 554 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 555 |         }
 556 |         let signalsSubscription = library.$signals.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:557:20: warning: no 'async' operations occur within 'await' expression
 555 |         }
 556 |         let signalsSubscription = library.$signals.sink { [weak self] _ in
 557 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 558 |         }
 559 |         itemsSubscription.store(in: &subscriptions)

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:562:20: warning: no 'async' operations occur within 'await' expression
 560 |         signalsSubscription.store(in: &subscriptions)
 561 |         library.$todayRefreshGeneration.sink { [weak self] _ in
 562 |             Task { await self?.libraryDidPublish() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 563 |         }.store(in: &subscriptions)
 564 |         library.$scanState.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:565:20: warning: no 'async' operations occur within 'await' expression
 563 |         }.store(in: &subscriptions)
 564 |         library.$scanState.sink { [weak self] _ in
 565 |             Task { await self?.scanStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 566 |         }.store(in: &subscriptions)
 567 |         library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:568:20: warning: no 'async' operations occur within 'await' expression
 566 |         }.store(in: &subscriptions)
 567 |         library.$refreshState.sink { [weak self] _ in
 568 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 569 |         }.store(in: &subscriptions)
 570 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2648:13: warning: result of call to 'openSelected' is unused [#no-usage]
2646 |             openWithDefaultApp(item)
2647 |         case .note, .reveal:
2648 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
2649 |         }
2650 |     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2680:17: warning: no 'async' operations occur within 'await' expression
2678 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
2679 |             Task {
2680 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
2681 |             }
2682 |         }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2707:17: warning: no 'async' operations occur within 'await' expression
2705 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
2706 |             Task {
2707 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
2708 |             }
2709 |         }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2765:17: warning: no 'async' operations occur within 'await' expression
2763 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
2764 |             Task {
2765 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
2766 |                     itemID: item.id,
2767 |                     title: item.title.text,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2796:17: warning: no 'async' operations occur within 'await' expression
2794 |         opener.openWithDefaultApp(pdf) { [weak self] error in
2795 |             Task {
2796 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
2797 |                     itemID: item.id,
2798 |                     title: item.title.text,
[157/175] Compiling BobMacCapture RefsRenameCardView.swift
[158/175] Compiling BobMacCapture RefsRowView.swift
[159/175] Compiling BobMacCapture RefsSearchBar.swift
[160/175] Compiling BobMacCapture RefsTabsViews.swift
[161/175] Compiling BobMacCapture RefsTodayLinkCardView.swift
[162/175] Compiling BobMacCapture RefsVisualTokens.swift
[163/175] Compiling BobMacCapture RefsHighlightsOpenKey.swift
[164/175] Compiling BobMacCapture RefsHighlightsTabsKey.swift
[165/175] Compiling BobMacCapture CapturePanelModel.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {
[166/175] Compiling BobMacCapture CapturePanelView.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {
[167/175] Compiling BobMacCapture CapturePanelWindowSizer.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {
[168/175] Compiling BobMacCapture CapturePickerFilterField.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {
[169/175] Compiling BobMacCapture CapturePickerState.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {
[170/175] Compiling BobMacCapture CapturePickerView.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {
[171/175] Compiling BobMacCapture CapturePlanBudgetMeterRow.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {
[172/175] Compiling BobMacCapture CapturePullInChoice.swift
/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-refs-panel-latency-1792418072-2997714/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {
[172/175] Write Objects.LinkFileList
[173/175] Linking BobMacCapture
[174/175] Applying BobMacCapture
Build complete! (77.90s)
Tests/BobMacCaptureTests/AppRelauncherTests.swift:12:13: warning: variable 'relauncher' was never mutated; consider changing to 'let' constant
 10 |         var spawnedArguments: [String]?
 11 | 
 12 |         var relauncher = AppRelauncher(
    |             `- warning: variable 'relauncher' was never mutated; consider changing to 'let' constant
 13 |             bundleURL: URL(fileURLWithPath: "/Applications/Bob Mac Capture.app"),
 14 |             processIdentifier: 4242,

Tests/BobMacCaptureTests/CaptureAgendaStoreTests.swift:76:31: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 74 | 
 75 |     private func recordArgv(_ url: URL) -> [String] {
 76 |         guard let text = try? String(contentsOf: url) else {
    |                               `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 77 |             return []
 78 |         }

Tests/BobMacCaptureTests/CaptureAgendaStoreTests.swift:324:13: warning: initialization of immutable value 'store' was never used; consider replacing with assignment to '_' or removing it [#no-usage]
322 |         let workspaceCenter = NotificationCenter()
323 |         let defaultCenter = NotificationCenter()
324 |         let store = try makeStore(
    |             `- warning: initialization of immutable value 'store' was never used; consider replacing with assignment to '_' or removing it [#no-usage]
325 |             recordURL: recordURL,
326 |             workspaceCenter: workspaceCenter,

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:206:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
204 |         XCTAssertNil(model.completionResponse)
205 |         XCTAssertNil(model.picker)
206 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
207 |         XCTAssertTrue(record.contains("argv=capture-rewrite --cursor 17 --format json -- Do work @file:id^"))
208 |         XCTAssertFalse(record.contains("capture-complete --all-tasks --cursor 17"))

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:300:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
298 |         XCTAssertEqual(textView.string, "Do work @file:id")
299 | 
300 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
301 |         let rewriteCount = record.components(separatedBy: "argv=capture-rewrite").count - 1
302 |         XCTAssertEqual(rewriteCount, 1)

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:321:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
319 | 
320 |         XCTAssertEqual(model.plainDraft, "Do work @file^id ")
321 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
322 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-rewrite").count - 1, 1)
323 |     }

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:425:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
423 |         XCTAssertEqual(model.statusText, "Pick a task or type a new ID — press Tab to browse")
424 |         XCTAssertEqual(model.plainDraft, "@file:")
425 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
426 |         XCTAssertTrue(record.contains("argv=capture-rewrite --cursor 6 --format json -- @file:"))
427 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 6 --format json -- @file:"))

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:455:27: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
453 |         try await Task.sleep(nanoseconds: 100_000_000)
454 |         XCTAssertFalse(model.pickerVisible)
455 |         let early = (try? String(contentsOf: recordURL)) ?? ""
    |                           `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
456 |         XCTAssertFalse(early.contains("argv=capture-complete"))
457 | 

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:478:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
476 |         XCTAssertEqual(model.plainDraft, "Do work @file^id")
477 |         XCTAssertNil(model.picker)
478 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
479 |         XCTAssertFalse(record.contains("capture-complete --all-tasks --cursor 17"))
480 |     }

Tests/BobMacCaptureTests/PlainTextPasteTests.swift:22:9: warning: no calls to throwing functions occur within 'try' expression
 20 |         // Regression guard for browser pasteboards: HTML/RTF source must never become
 21 |         // literal capture text when a plain-text flavor is available.
 22 |         try withScratchPasteboard { pasteboard in
    |         `- warning: no calls to throwing functions occur within 'try' expression
 23 |             writeRichAndPlainPasteboard(pasteboard, plain: "Plain capture text")
 24 | 

Tests/BobMacCaptureTests/PlainTextPasteTests.swift:278:9: warning: no calls to throwing functions occur within 'try' expression
276 |         // Regression guard for responder-chain fallthrough: plain-text paste only
277 |         // consumes events when the target is an editable text view.
278 |         try withScratchPasteboard { pasteboard in
    |         `- warning: no calls to throwing functions occur within 'try' expression
279 |             writeRichAndPlainPasteboard(pasteboard, plain: "inserted")
280 | 

Tests/BobMacCaptureTests/RefsPanelModelTests.swift:3894:24: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3892 | /// How many fake-bob invocations start with `prefix` in a record file.
3893 | private func argvCount(_ recordURL: URL, prefix: String) -> Int {
3894 |     let record = (try? String(contentsOf: recordURL)) ?? ""
     |                        `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3895 |     return record.components(separatedBy: prefix).count - 1
3896 | }

Tests/BobMacCaptureTests/CaptureParentTaskPanelTests.swift:361:20: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
359 |         await waitUntil { model.pickerVisible }
360 |         await waitUntil {
361 |             ((try? String(contentsOf: recordURL)) ?? "").contains(
    |                    `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
362 |                 "argv=capture --dry-run --no-clip --format json -- +\n"
363 |             )

Tests/BobMacCaptureTests/CaptureParentTaskPanelTests.swift:391:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
389 |         XCTAssertEqual(model.picker?.candidates.count, 8)
390 |         XCTAssertEqual(model.pickerPresentation?.mode, .filtered)
391 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
392 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 2)
393 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 0 "))

Tests/BobMacCaptureTests/CaptureParentTaskPanelTests.swift:454:20: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
452 |         model.editorTextDidChange(cursorUTF8Offset: 15)
453 |         await waitUntil {
454 |             ((try? String(contentsOf: recordURL)) ?? "").contains(
    |                    `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
455 |                 "argv=capture-complete --all-tasks --cursor 15 --format json -- @cash+goog-exit"
456 |             )

Tests/BobMacCaptureTests/CaptureTaskGotoPanelTests.swift:283:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
281 |         XCTAssertEqual(model.statusText, "Pick a task to open — press Tab to browse")
282 |         XCTAssertEqual(model.previewState, .idle)
283 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
284 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 1)
285 |         XCTAssertFalse(record.contains("argv=capture --"))

Tests/BobMacCaptureTests/CaptureTaskGotoPanelTests.swift:303:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
301 |         XCTAssertTrue(model.pickerSourceIsTaskGoto)
302 |         XCTAssertEqual(model.picker?.candidates.count, 8)
303 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
304 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 1)
305 |     }

Tests/BobMacCaptureTests/CaptureTaskGotoPanelTests.swift:317:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
315 |         XCTAssertEqual(model.picker?.candidates.count, 1)
316 |         XCTAssertEqual(model.picker?.snapshotIsPartial, true)
317 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
318 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 2)
319 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 0 "))

Tests/BobMacCaptureTests/CaptureTaskGotoPanelTests.swift:346:30: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
344 |             XCTAssertFalse(model.hasDraft)
345 |             XCTAssertTrue(model.stashEntries.isEmpty)
346 |             let record = try String(contentsOf: recordURL)
    |                              `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
347 |             XCTAssertFalse(record.contains("argv=capture --"))
348 |             XCTAssertFalse(record.contains("argv=capture-task-id"))

Tests/BobMacCaptureTests/CaptureTaskGotoPanelTests.swift:367:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
365 |         XCTAssertEqual(opened, [expectedURL(line: 7, ref: "7:446bd057")])
366 |         XCTAssertFalse(model.taskIDPromptVisible)
367 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
368 |         XCTAssertFalse(record.contains("argv=capture-task-id"))
369 |         XCTAssertFalse(record.contains("argv=capture --"))

Tests/BobMacCaptureTests/RefsInspectorTests.swift:383:16: warning: no 'async' operations occur within 'await' expression
 381 |     let root = FileManager.default.temporaryDirectory
 382 |       .appendingPathComponent(UUID().uuidString)
 383 |     let slow = await RefsPDFIntrinsicsLoader(
     |                `- warning: no 'async' operations occur within 'await' expression
 384 |       cacheDirectory: root,
 385 |       reader: { @Sendable _ in

Tests/BobMacCaptureTests/RefsInspectorTests.swift:401:16: warning: no 'async' operations occur within 'await' expression
 399 |     // The abandoned read never queues later loads behind it: a
 400 |     // fresh loader answers at once.
 401 |     let fast = await RefsPDFIntrinsicsLoader(
     |                `- warning: no 'async' operations occur within 'await' expression
 402 |       cacheDirectory: root,
 403 |       reader: { @Sendable _ in RefsPDFIntrinsics(pageCount: 3) }

Tests/BobMacCaptureTests/RefsInspectorTests.swift:414:18: warning: no 'async' operations occur within 'await' expression
 412 |     let root = FileManager.default.temporaryDirectory
 413 |       .appendingPathComponent(UUID().uuidString)
 414 |     let loader = await RefsPDFIntrinsicsLoader(
     |                  `- warning: no 'async' operations occur within 'await' expression
 415 |       cacheDirectory: root,
 416 |       reader: { @Sendable _ in

Tests/BobMacCaptureTests/RefsInspectorTests.swift:499:18: warning: no 'async' operations occur within 'await' expression
 497 |     let root = FileManager.default.temporaryDirectory
 498 |       .appendingPathComponent(UUID().uuidString)
 499 |     let loader = await RefsPDFIntrinsicsLoader(
     |                  `- warning: no 'async' operations occur within 'await' expression
 500 |       cacheDirectory: root,
 501 |       reader: { @Sendable _ in

Tests/BobMacCaptureTests/CaptureAgendaModelTests.swift:486:19: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
484 |         typeDraft(model, "=")
485 |         await waitUntil {
486 |             (try? String(contentsOf: recordURL))?.components(separatedBy: "argv=")
    |                   `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
487 |                 .dropFirst()
488 |                 .contains { !$0.hasPrefix("capture-templates") } == true

Tests/BobMacCaptureTests/CaptureAgendaModelTests.swift:632:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
630 |         assertIdleAgendaVisible(model)
631 | 
632 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
633 |         let mutating = record.split(whereSeparator: \.isNewline).filter { line in
634 |             line.hasPrefix("argv=capture ") && !line.contains("--dry-run")

Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:11:13: warning: variable 'loading' was never mutated; consider changing to 'let' constant
  9 | final class RefsTodayLinkCardDesignTests: XCTestCase {
 10 |     func testTodayCardStateMatrixAndToastFixturesToPNG() throws {
 11 |         var loading = makeCard()
    |             `- warning: variable 'loading' was never mutated; consider changing to 'let' constant
 12 | 
 13 |         var ready = makeCard()

Tests/BobMacCaptureTests/CapturePanelAgendaLayoutTests.swift:432:19: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
430 |         typeDraft(model, "=")
431 |         await waitUntil {
432 |             (try? String(contentsOf: recordURL))?.components(separatedBy: "argv=")
    |                   `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
433 |                 .dropFirst()
434 |                 .contains { !$0.hasPrefix("capture-templates") } == true

Tests/BobMacCaptureTests/RefsEntryPointsTests.swift:836:28: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
834 | 
835 |     private func entryPointsPlanCount(_ recordURL: URL) -> Int {
836 |         let record = (try? String(contentsOf: recordURL)) ?? ""
    |                            `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
837 |         return record.components(separatedBy: "argv=plan -f json").count - 1
838 |     }

Tests/BobMacCaptureTests/RefsLibraryTests.swift:103:14: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 101 |     // its invocation before asserting on the record.
 102 |     await waitUntil(timeout: 15) {
 103 |       ((try? String(contentsOf: recordURL)) ?? "")
     |              `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 104 |         .contains("argv=ref list -R all -A -f json -g")
 105 |     }

Tests/BobMacCaptureTests/RefsLibraryTests.swift:188:14: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 186 |     // stays published and the state never flips to failed.
 187 |     await waitUntil(timeout: 15) {
 188 |       ((try? String(contentsOf: recordURL)) ?? "").contains("-g")
     |              `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 189 |     }
 190 |     try? await Task.sleep(nanoseconds: 2_000_000_000)

Tests/BobMacCaptureTests/RefsLibraryTests.swift:217:24: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 215 |       }
 216 |     }
 217 |     let launches = try String(contentsOf: recordURL)
     |                        `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 218 |       .components(separatedBy: "argv=ref list").count
 219 | 

Tests/BobMacCaptureTests/RefsLibraryTests.swift:223:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 221 | 
 222 |     await waitUntil(timeout: 15) {
 223 |       let record = (try? String(contentsOf: recordURL)) ?? ""
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 224 |       return record.components(separatedBy: "argv=ref list").count > launches
 225 |     }

Tests/BobMacCaptureTests/RefsLibraryTests.swift:241:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 239 |     await waitUntil(timeout: 15) { context.library.lastSuccessAt != nil }
 240 | 
 241 |     let record = try String(contentsOf: recordURL)
     |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 242 |     XCTAssertFalse(record.contains("-g"))
 243 |   }

Tests/BobMacCaptureTests/RefsLibraryTests.swift:262:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 260 |     // only runs when needed.
 261 |     await waitUntil(timeout: 40) {
 262 |       let record = (try? String(contentsOf: recordURL)) ?? ""
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 263 |       return record.components(separatedBy: "argv=ref list").count == 4
 264 |     }

Tests/BobMacCaptureTests/RefsLibraryTests.swift:266:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 264 |     }
 265 |     try? await Task.sleep(nanoseconds: 4_000_000_000)
 266 |     let record = try String(contentsOf: recordURL)
     |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 267 |     XCTAssertEqual(record.components(separatedBy: "argv=ref list").count, 4)
 268 |     XCTAssertEqual(record.components(separatedBy: "argv=plan -f json").count, 3)

Tests/BobMacCaptureTests/RefsLibraryTests.swift:308:28: error: cannot find 'RefsNewestTests' in scope
 306 |         $0.id == "ref/blogs/small_opened.md"
 307 |           && $0.added == RefDay(year: 2026, month: 9, day: 11)
 308 |           && $0.addedAt == RefsNewestTests.instant("2026-09-11T19:12:00Z")
     |                            `- error: cannot find 'RefsNewestTests' in scope
 309 |       }
 310 |     )

Tests/BobMacCaptureTests/RefsLibraryTests.swift:304:5: error: the compiler is unable to type-check this expression in reasonable time; try breaking up the expression into distinct sub-expressions
 302 |     try? await Task.sleep(nanoseconds: 300_000_000)
 303 | 
 304 |     XCTAssertTrue(
     |     `- error: the compiler is unable to type-check this expression in reasonable time; try breaking up the expression into distinct sub-expressions
 305 |       context.library.items.contains {
 306 |         $0.id == "ref/blogs/small_opened.md"

Tests/BobMacCaptureTests/RefsLibraryTests.swift:315:28: error: cannot find 'RefsNewestTests' in scope
 313 |         $0.id == "ref/books/small_book.md"
 314 |           && $0.added == RefDay(year: 2026, month: 8, day: 30)
 315 |           && $0.addedAt == RefsNewestTests.instant("2026-08-30T19:12:00Z")
     |                            `- error: cannot find 'RefsNewestTests' in scope
 316 |       }
 317 |     )

Tests/BobMacCaptureTests/RefsLibraryTests.swift:311:5: error: the compiler is unable to type-check this expression in reasonable time; try breaking up the expression into distinct sub-expressions
 309 |       }
 310 |     )
 311 |     XCTAssertTrue(
     |     `- error: the compiler is unable to type-check this expression in reasonable time; try breaking up the expression into distinct sub-expressions
 312 |       context.library.items.contains {
 313 |         $0.id == "ref/books/small_book.md"

Tests/BobMacCaptureTests/RefsLibraryTests.swift:353:28: error: cannot find 'RefsNewestTests' in scope
 351 |         $0.id == "ref/blogs/small_opened.md"
 352 |           && $0.added == RefDay(year: 2026, month: 9, day: 11)
 353 |           && $0.addedAt == RefsNewestTests.instant("2026-09-11T19:12:00Z")
     |                            `- error: cannot find 'RefsNewestTests' in scope
 354 |       }
 355 |     )

Tests/BobMacCaptureTests/RefsLibraryTests.swift:349:5: error: the compiler is unable to type-check this expression in reasonable time; try breaking up the expression into distinct sub-expressions
 347 |     try? await Task.sleep(nanoseconds: 300_000_000)
 348 | 
 349 |     XCTAssertTrue(
     |     `- error: the compiler is unable to type-check this expression in reasonable time; try breaking up the expression into distinct sub-expressions
 350 |       context.library.items.contains {
 351 |         $0.id == "ref/blogs/small_opened.md"

Tests/BobMacCaptureTests/RefsLibraryTests.swift:360:28: error: cannot find 'RefsNewestTests' in scope
 358 |         $0.id == "ref/books/small_book.md"
 359 |           && $0.added == RefDay(year: 2026, month: 8, day: 30)
 360 |           && $0.addedAt == RefsNewestTests.instant("2026-08-30T19:12:00Z")
     |                            `- error: cannot find 'RefsNewestTests' in scope
 361 |       }
 362 |     )

Tests/BobMacCaptureTests/RefsLibraryTests.swift:356:5: error: the compiler is unable to type-check this expression in reasonable time; try breaking up the expression into distinct sub-expressions
 354 |       }
 355 |     )
 356 |     XCTAssertTrue(
     |     `- error: the compiler is unable to type-check this expression in reasonable time; try breaking up the expression into distinct sub-expressions
 357 |       context.library.items.contains {
 358 |         $0.id == "ref/books/small_book.md"

Tests/BobMacCaptureTests/RefsLibraryTests.swift:388:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 386 |     context.library.refreshToday(reason: .manual)
 387 |     await waitUntil(timeout: 15) {
 388 |       let record = (try? String(contentsOf: recordURL)) ?? ""
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 389 |       return record.components(separatedBy: "argv=plan -f json").count == 3
 390 |     }

Tests/BobMacCaptureTests/RefsLibraryTests.swift:463:27: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 461 |       }
 462 |     }
 463 |     let staleRecord = try String(contentsOf: recordURL)
     |                           `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 464 |     let count = staleRecord.components(separatedBy: "argv=").count
 465 | 

Tests/BobMacCaptureTests/RefsLibraryTests.swift:468:27: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 466 |     context.library.refreshIfStale()
 467 |     try? await Task.sleep(nanoseconds: 1_000_000_000)
 468 |     let quietRecord = try String(contentsOf: recordURL)
     |                           `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 469 |     XCTAssertEqual(quietRecord.components(separatedBy: "argv=").count, count)
 470 | 

Tests/BobMacCaptureTests/RefsLibraryTests.swift:474:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 472 |     context.library.refreshIfStale()
 473 |     await waitUntil(timeout: 15) {
 474 |       let record = (try? String(contentsOf: recordURL)) ?? ""
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 475 |       return record.components(separatedBy: "argv=").count > count
 476 |     }

Tests/BobMacCaptureTests/RefsLibraryTests.swift:494:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 492 |       return false
 493 |     }
 494 |     let record = try String(contentsOf: recordURL)
     |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 495 |     XCTAssertEqual(
 496 |       record.components(separatedBy: "argv=ref scan -w -f json").count - 1,

Tests/BobMacCaptureTests/RefsLibraryTests.swift:524:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 522 |       return false
 523 |     }
 524 |     let record = try String(contentsOf: recordURL)
     |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 525 |     XCTAssertEqual(
 526 |       record.components(separatedBy: "argv=ref scan -w -f json").count - 1,

Tests/BobMacCaptureTests/RefsLibraryTests.swift:562:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 560 |         $0.id == "ref/papers/harness_notes.md"
 561 |       })
 562 |     let record = try String(contentsOf: recordURL)
     |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 563 |     guard let scanRange = record.range(of: "argv=ref scan -w -f json"),
 564 |       let listRange = record.range(of: "argv=ref list -R all -A -f json")

Tests/BobMacCaptureTests/RefsLibraryTests.swift:586:27: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 584 |     context.library.handleWatcherChange()
 585 |     try? await Task.sleep(nanoseconds: 500_000_000)
 586 |     let midRecord = (try? String(contentsOf: recordURL)) ?? ""
     |                           `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 587 |     XCTAssertFalse(midRecord.contains("argv=ref list"))
 588 |     await waitUntil(timeout: 15) {

Tests/BobMacCaptureTests/RefsLibraryTests.swift:595:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 593 |     }
 594 |     try? await Task.sleep(nanoseconds: 500_000_000)
 595 |     let record = try String(contentsOf: recordURL)
     |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 596 |     XCTAssertEqual(
 597 |       record.components(separatedBy: "argv=ref list -R all -A -f json").count - 1,

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:639:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 637 |         XCTAssertEqual(model.lastSuccess?.toggleBehavior, "ensure_next")
 638 |         XCTAssertEqual(model.lastSuccess?.pomodoroLinkAction, "moved")
 639 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 640 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- @file+goog-exit"))
 641 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- @file+goog-exit"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:678:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 676 |         XCTAssertNil(model.lastSuccess?.toggleBehavior)
 677 |         XCTAssertEqual(model.lastSuccess?.toggleDirection, "next")
 678 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 679 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- @file+goog-exit!"))
 680 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- @file+goog-exit!"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:755:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 753 |         XCTAssertTrue(model.previewResults.isEmpty)
 754 |         XCTAssertEqual(model.statusText, "Pick an active task — press Tab to browse")
 755 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 756 |         XCTAssertFalse(record.contains("argv=capture --dry-run"))
 757 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 1)

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:785:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 783 |         XCTAssertEqual(model.statusText, "Pick any open task — press Tab to browse")
 784 |         XCTAssertEqual(model.previewState, .idle)
 785 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 786 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 1)
 787 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:814:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 812 |         XCTAssertEqual(model.picker?.source, .taskLink)
 813 |         XCTAssertEqual(model.picker?.candidates.count, 8)
 814 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 815 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 1)
 816 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:845:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 843 |         XCTAssertEqual(model.picker?.candidates.count, 8)
 844 |         XCTAssertNil(model.completionResponse)
 845 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 846 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 11 --format json -- "))
 847 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:867:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 865 |         await waitUntil { model.pickerVisible }
 866 | 
 867 |         let before = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 868 |         XCTAssertEqual(before.components(separatedBy: "argv=capture-complete").count - 1, 1)
 869 | 

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:876:25: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 874 |         XCTAssertEqual(model.picker?.filterText, "deep")
 875 |         XCTAssertEqual(model.pickerPresentation?.mode, .filtered)
 876 |         let after = try String(contentsOf: recordURL)
     |                         `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 877 |         XCTAssertEqual(after.components(separatedBy: "argv=capture-complete").count - 1, 1)
 878 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:887:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 885 | 
 886 |         XCTAssertEqual(model.picker?.source, .taskLink)
 887 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 888 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 1)
 889 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:908:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 906 |         XCTAssertEqual(model.picker?.snapshotIsPartial, true)
 907 |         XCTAssertEqual(model.pickerPresentation?.mode, .filtered)
 908 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 909 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 2)
 910 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 0 "))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:952:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 950 |         XCTAssertFalse(model.pickerVisible)
 951 |         XCTAssertEqual(model.lastSuccess?.kind, "pomodoro_link")
 952 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 953 |         XCTAssertTrue(record.contains("argv=capture --format json --require-pull-in-choice --refuse-override -- @sase:deep-fix"))
 954 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1035:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1033 | 
1034 |         XCTAssertEqual(model.collapsedSelectionUTF8Offset(), 21)
1035 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1036 |         XCTAssertTrue(
1037 |             record.contains(

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1067:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1065 | 
1066 |         XCTAssertEqual(model.lastSuccess?.kind, "pomodoro_link")
1067 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1068 |         XCTAssertTrue(record.contains("argv=capture --format json --require-pull-in-choice --refuse-override -- @sase:fix-flaky-gkeep"))
1069 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1092:17: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1090 |         XCTAssertEqual(openedURL?.host, "bob-open-notes")
1091 |         XCTAssertTrue(
1092 |             try String(contentsOf: recordURL).contains(
     |                 `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1093 |                 "argv=capture --format json --require-pull-in-choice --refuse-override -- @sase:fix-flaky-gkeep"
1094 |             )

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1138:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1136 |         XCTAssertEqual(model.picker?.snapshotIsPartial, false)
1137 |         XCTAssertEqual(model.pickerPresentation?.mode, .filtered)
1138 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1139 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 2)
1140 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 1 "))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1240:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1238 |         XCTAssertFalse(model.pickerChipVisible)
1239 |         XCTAssertNil(model.completionResponse)
1240 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1241 |         XCTAssertTrue(
1242 |             record.contains("argv=capture --dry-run --no-clip --format json -- ^sase:deep-fix")

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1502:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1500 |         XCTAssertEqual(model.statusText, "Pick a task or type a new ID — press Tab to browse")
1501 |         XCTAssertEqual(model.previewState, .idle)
1502 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1503 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- @file:"))
1504 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 6 --format json -- @file:"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1529:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1527 |         XCTAssertEqual(model.picker?.snapshotIsPartial, false)
1528 |         XCTAssertEqual(model.pickerPresentation?.mode, .filtered)
1529 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1530 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 6 --format json -- @file:rea"))
1531 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1803:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1801 |         XCTAssertFalse(model.pickerVisible)
1802 |         XCTAssertTrue(model.completionVisible)
1803 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1804 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 23 --format json -- Follow up @file:new-id#"))
1805 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2305:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2303 |             "Closed CAPTURE · 1 started · 3 Work Log entries"
2304 |         )
2305 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2306 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- \(draft)"))
2307 |         XCTAssertTrue(record.contains("argv=capture --format json --require-pull-in-choice --refuse-override -- \(draft)"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2452:30: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2450 |             model.submit(openAfterCapture: false)
2451 |             await waitUntil { !model.isSubmitting }
2452 |             let record = try String(contentsOf: recordURL)
     |                              `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2453 |             XCTAssertTrue(
2454 |                 record.contains("argv=capture --dry-run --no-clip --format json -- \(draft)"),

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2502:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2500 |         model.submit(openAfterCapture: false)
2501 |         XCTAssertFalse(model.isSubmitting)
2502 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2503 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- x*1\n"))
2504 |         XCTAssertFalse(record.contains("argv=capture --format json --require-pull-in-choice --refuse-override -- x*1,"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2942:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2940 |         XCTAssertFalse(model.isSubmitting)
2941 |         XCTAssertEqual(model.statusText, "Type a task number after ~ — Start is disabled")
2942 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2943 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- =\n"))
2944 |         XCTAssertFalse(record.contains("argv=capture --format json --require-pull-in-choice --refuse-override -- =~"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2991:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2989 |         XCTAssertFalse(model.isSubmitting)
2990 |         XCTAssertEqual(model.statusText, "Type a task number after , — Close is disabled")
2991 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2992 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- x1\n"))
2993 |         XCTAssertFalse(record.contains("argv=capture --format json --require-pull-in-choice --refuse-override -- x1,"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3038:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3036 |         model.submit(openAfterCapture: false)
3037 |         XCTAssertFalse(model.isSubmitting)
3038 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3039 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- x\n"))
3040 |         XCTAssertFalse(record.contains("argv=capture --format json --require-pull-in-choice --refuse-override -- x\n- 1"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3086:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3084 |             ["sketched the URL parser"]
3085 |         )
3086 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3087 |         XCTAssertTrue(
3088 |             record.contains(

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3164:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3162 |             "Started CAPTURE 0945-1010 (25m) at line 4"
3163 |         )
3164 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3165 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- \(draft)"))
3166 |         XCTAssertTrue(record.contains("argv=capture --format json --require-pull-in-choice --refuse-override -- \(draft)"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3243:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3241 |             "Restarted CAPTURE 0920-0945 → 0935-1000 (25m) at line 5"
3242 |        FAIL BobMacCaptureTests
 )
3243 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3244 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- \(draft)"))
3245 |         XCTAssertTrue(record.contains("argv=capture --format json --require-pull-in-choice -- \(draft)"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3267:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3265 |         await waitUntil { !model.isSubmitting }
3266 | 
3267 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3268 |         XCTAssertTrue(record.contains("argv=capture --format json --require-pull-in-choice --refuse-override -- ="))
3269 |         XCTAssertFalse(record.contains("argv=capture --dry-run"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3293:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3291 |         XCTAssertEqual(model.plainDraft, "")
3292 |         XCTAssertTrue(model.processClient?.refuseOverrideKnownUnsupported == true)
3293 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3294 |         let invocations = Array(record.components(separatedBy: "argv=capture").dropFirst())
3295 |         XCTAssertEqual(invocations.count, 2)

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3374:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3372 |         await waitUntil { !model.isSubmitting }
3373 | 
3374 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3375 |         XCTAssertTrue(
3376 |             record.contains("argv=capture --format json --require-pull-in-choice --refuse-override -- \(stale)")

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3473:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3471 |         XCTAssertEqual(model.completionResponse?.candidates.count, 4)
3472 |         XCTAssertEqual(model.completionResponse?.candidates.first?.replacement, "bugs")
3473 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3474 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 2 --format json -- =#"))
3475 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3524:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3522 |             CaptureRange(start: 4, end: 6)
3523 |         )
3524 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3525 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 6 --format json -- x =#de"))
3526 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3550:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3548 |         XCTAssertNil(model.completionResponse)
3549 |         XCTAssertFalse(model.completionVisible)
3550 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3551 |         XCTAssertFalse(record.contains("argv=capture-complete"))
3552 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3577:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3575 |         XCTAssertEqual(model.statusText, "Pick a Pomodoro to start, or type a new name")
3576 |         XCTAssertTrue(model.completionVisible)
3577 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3578 |         XCTAssertFalse(record.contains("argv=capture --dry-run"))
3579 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3866:30: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3864 |         XCTAssertNotNil(model.closePresentation)
3865 |         let dryRunLine = "argv=capture --dry-run --no-clip --format json -- x"
3866 |         let runsBefore = try String(contentsOf: recordURL)
     |                              `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3867 |             .components(separatedBy: dryRunLine).count - 1
3868 |         XCTAssertEqual(runsBefore, 1)

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3877:30: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3875 |                 return false
3876 |             }
3877 |             let runs = (try? String(contentsOf: recordURL))?
     |                              `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3878 |                 .components(separatedBy: dryRunLine).count ?? 1
3879 |             return runs - 1 == 2

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4045:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4043 | 
4044 |         XCTAssertEqual(model.lastSuccess?.pomodoroStart?.durationMinutes, 15)
4045 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4046 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- \(draft)"))
4047 |         XCTAssertTrue(record.contains("argv=capture --format json --require-pull-in-choice --refuse-override -- \(draft)"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4108:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4106 |         XCTAssertEqual(model.lastSuccess?.pomodoroAdjust?.deltaMinutes, 25)
4107 |         XCTAssertFalse(model.lastSuccess?.dryRun ?? true)
4108 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4109 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- \(draft)"))
4110 |         XCTAssertTrue(record.contains("argv=capture --format json --require-pull-in-choice --refuse-override -- \(draft)"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4401:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4399 |         XCTAssertEqual(model.lastSuccess?.toggleBehavior, "ensure_next")
4400 |         XCTAssertEqual(model.lastSuccess?.pomodoroLinkAction, "moved")
4401 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4402 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- @file+goog-exit#coding"))
4403 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- @file+goog-exit#coding"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4702:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4700 |         }
4701 | 
4702 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4703 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- Restored café @Cash\n- child"))
4704 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- Restored café @Cash\n- child"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4767:28: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4765 |         await waitUntil { !model.isSubmitting }
4766 | 
4767 |         let record = (try? String(contentsOf: recordURL)) ?? ""
     |                            `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4768 |         let invocationCount = record.components(separatedBy: "argv=")
4769 |             .dropFirst()

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4793:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4791 |         XCTAssertEqual(model.plainDraft, "Call bank @Cash")
4792 |         XCTAssertTrue(model.previewResult?.dryRun ?? false)
4793 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4794 |         XCTAssertTrue(record.contains("--dry-run"))
4795 |         XCTAssertFalse(record.contains("--no-clip"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4829:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4827 | 
4828 |         XCTAssertEqual(model.collapsedSelectionUTF8Offset(), "Buy milk @@dev".utf8.count)
4829 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4830 |         XCTAssertTrue(record.contains("argv=capture-rewrite --cursor 16 --format json -- Buy milk @dev @@"))
4831 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4854:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4852 | 
4853 |         XCTAssertEqual(model.plainDraft, "Buy milk @dev @@ and keep typing")
4854 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4855 |         XCTAssertTrue(record.contains("argv=capture-rewrite --cursor 16 --format json -- Buy milk @dev @@"))
4856 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4888:20: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4886 |         model.editorTextDidChange(cursorUTF8Offset: model.plainDraft.utf8.count)
4887 |         await waitUntil {
4888 |             ((try? String(contentsOf: recordURL)) ?? "").contains("argv=capture-parse")
     |                    `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4889 |         }
4890 | 

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4894:20: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4892 |         model.editorTextDidChange(cursorUTF8Offset: model.plainDraft.utf8.count)
4893 |         await waitUntil {
4894 |             ((try? String(contentsOf: recordURL)) ?? "").contains("Buy milk @dev @@@")
     |                    `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4895 |         }
4896 | 

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4897:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4895 |         }
4896 | 
4897 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4898 |         XCTAssertFalse(record.contains("capture-rewrite"))
4899 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4933:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4931 | 
4932 |         XCTAssertNil(model.completionResponse)
4933 |         var record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4934 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 1)
4935 |         XCTAssertTrue(

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4950:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4948 |             CaptureRange(start: 6, end: 16)
4949 |         )
4950 |         record = try String(contentsOf: recordURL)
     |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4951 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 2)
4952 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4978:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4976 |         XCTAssertEqual(model.collapsedSelectionUTF8Offset(), "prefix [[AI".utf8.count)
4977 |         XCTAssertEqual(model.statusText, "Link completion warning: skipped unreadable note")
4978 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4979 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 11 --format json -- prefix [[AI suffix"))
4980 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5059:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5057 |         XCTAssertEqual(model.completionResponse?.replacement, CaptureRange(start: 6, end: 8))
5058 |         XCTAssertEqual(model.completionResponse?.candidates.first?.route, "mac_inbox")
5059 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5060 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- idea @ma^new-id"))
5061 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- idea @ma^new-id"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5096:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5094 |         XCTAssertEqual(model.completionResponse?.replacement, CaptureRange(start: 6, end: 8))
5095 |         XCTAssertEqual(model.completionResponse?.candidates.first?.route, "mac_inbox")
5096 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5097 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- idea @ma"))
5098 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- idea @ma"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5134:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5132 |         XCTAssertEqual(model.completionResponse?.replacement, CaptureRange(start: 2, end: 4))
5133 |         XCTAssertEqual(model.completionResponse?.candidates.first?.route, "mac_inbox")
5134 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5135 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- \(draft)"))
5136 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- \(draft)"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5237:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5235 |         XCTAssertEqual(preview.blockID, "new-id")
5236 |         XCTAssertNil(preview.dayFile)
5237 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5238 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- idea @mac_inbox^new-id"))
5239 |         XCTAssertTrue(record.contains("capture-complete"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5264:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5262 | 
5263 |         XCTAssertNil(model.completionResponse)
5264 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5265 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- prefix [[AI suffix"))
5266 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- prefix [[AI suffix"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5297:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5295 |         XCTAssertEqual(model.lastSuccess?.blockID, "parent-id")
5296 | 
5297 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5298 |         XCTAssertTrue(record.contains("argv=capture --format json --require-pull-in-choice --refuse-override -- Follow up @file^new-id"))
5299 |         XCTAssertTrue(record.contains("argv=capture --format json --require-pull-in-choice --refuse-override -- Add context @file+parent-id"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5360:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5358 |         XCTAssertEqual(model.completionResponse?.replacement, CaptureRange(start: 11, end: 15))
5359 | 
5360 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5361 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- Add context @file+parent-id"))
5362 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- Add context @file+parent-id"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5392:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5390 |         XCTAssertEqual(model.completionResponse?.replacement, CaptureRange(start: 1, end: 1))
5391 |         XCTAssertEqual(model.completionResponse?.candidates.first?.route, "file")
5392 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5393 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- @"))
5394 |         XCTAssertFalse(record.contains("capture-complete"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5422:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5420 |         XCTAssertEqual(model.completionResponse?.replacement, CaptureRange(start: 1, end: 3))
5421 |         XCTAssertEqual(model.completionResponse?.candidates.map(\.route), ["file"])
5422 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5423 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- @fi"))
5424 |         XCTAssertFalse(record.contains("capture-complete"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5451:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5449 |         XCTAssertEqual(model.completionResponse?.replacement, CaptureRange(start: 1, end: 3))
5450 |         XCTAssertEqual(model.completionResponse?.candidates.first?.route, "file")
5451 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5452 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- @fi"))
5453 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 3 --format json -- @fi"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5491:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5489 |         XCTAssertEqual(model.plainDraft, "@file+goog-exit")
5490 |         XCTAssertNil(model.completionResponse)
5491 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5492 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 6 --format json -- @file+"))
5493 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5525:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5523 | 
5524 |         await waitUntil { model.completionResponse?.context == "task" }
5525 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5526 |         XCTAssertTrue(
5527 |             record.contains("argv=capture-complete --all-tasks --cursor 16 --format json -- Call bank @cash+")

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5562:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5560 | 
5561 |         await waitUntil { model.completionResponse?.context == "task" }
5562 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5563 |         XCTAssertTrue(
5564 |             record.contains("argv=capture-complete --all-tasks --cursor 16 --format json -- Call bank @Cash+")

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5602:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5600 | 
5601 |         await waitUntil { model.completionResponse?.context == "task" }
5602 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5603 |         XCTAssertTrue(
5604 |             record.contains("argv=capture-complete --all-tasks --cursor 17 --format json -- Add note @design+")

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5717:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5715 | 
5716 |         await waitUntil { model.completionResponse?.context == "task" }
5717 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5718 |         XCTAssertTrue(
5719 |             record.contains(

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5754:32: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5752 | 
5753 |         await waitUntil {
5754 |             let record = (try? String(contentsOf: recordURL)) ?? ""
     |                                `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5755 |             return record.contains("argv=capture-complete --all-tasks --cursor 16 --format json -- Call bank @Cash+")
5756 |         }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5758:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5756 |         }
5757 | 
5758 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5759 |         XCTAssertFalse(record.contains("argv=capture-complete --all-tasks --cursor 15"))
5760 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5791:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5789 | 
5790 |         XCTAssertEqual(model.completionResponse?.candidates.first?.route, "mac_inbox")
5791 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5792 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 8 --format json -- idea @ma"))
5793 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5822:32: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5820 |         model.editorTextDidChange(cursorUTF8Offset: model.plainDraft.utf8.count)
5821 |         await waitUntil {
5822 |             let record = (try? String(contentsOf: recordURL)) ?? ""
     |                                `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5823 |             return record.contains("argv=capture-complete --all-tasks --cursor 16 --format json -- Call bank @Cash+")
5824 |         }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5826:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5824 |         }
5825 | 
5826 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5827 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- Call bank @Cash+"))
5828 |         XCTAssertTrue(

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5862:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5860 |         XCTAssertEqual(model.completionResponse?.candidates.first?.blockID, "goog-exit")
5861 |         XCTAssertTrue(model.completionVisible)
5862 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5863 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 15 --format json -- note @Cash+goog"))
5864 | 

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5904:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5902 |         XCTAssertEqual(model.completionResponse?.candidates.first?.blockID, "bar")
5903 |         XCTAssertEqual(model.completionResponse?.candidates.first?.childCount, 2)
5904 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5905 |         XCTAssertTrue(
5906 |             record.contains(

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5946:32: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5944 |                 return false
5945 |             }
5946 |             let record = (try? String(contentsOf: recordURL)) ?? ""
     |                                `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5947 |             return record.contains("argv=capture-parse --format json -- jot idea #")
5948 |                 && record.contains("argv=capture --dry-run --no-clip --format json -- jot idea #")

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5956:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5954 |         XCTAssertNil(model.completionResponse)
5955 |         XCTAssertFalse(model.completionVisible)
5956 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5957 |         XCTAssertFalse(record.contains("capture-complete"))
5958 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5978:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5976 |         XCTAssertTrue(model.completionVisible)
5977 |         XCTAssertEqual(model.completionResponse?.candidates.first?.title, "Ideas")
5978 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5979 |         XCTAssertTrue(
5980 |             record.contains(

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6127:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6125 |         XCTAssertEqual(livePreview.normalizedCaptures.map(\.kind), ["task", "sub_bullet"])
6126 | 
6127 |         var record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6128 |         XCTAssertTrue(
6129 |             record.contains("argv=capture-complete --all-tasks --cursor 43 --format json -- ")

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6153:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6151 |         XCTAssertEqual(model.lastSuccessResults.map(\.text), ["Plan café", "File follow-up"])
6152 | 
6153 |         record = try String(contentsOf: recordURL)
     |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6154 |         XCTAssertEqual(
6155 |             record.components(separatedBy: "argv=capture --format json --dry-run -- ").count - 1,

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6225:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6223 |         XCTAssertEqual(focusEvents.last?.cursor, "note @Cash+new-id".utf8.count)
6224 |         XCTAssertFalse(model.editorInputLocked)
6225 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6226 |         XCTAssertTrue(
6227 |             record.contains("argv=capture-task-id --route cash --task-ref 8:missingidea --block-id new-id --format json")

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6454:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6452 |             return false
6453 |         }
6454 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6455 |         XCTAssertFalse(record.contains("capture-pomodoro-name"))
6456 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- "))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6497:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6495 |             return false
6496 |         }
6497 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6498 |         XCTAssertFalse(record.contains("capture-pomodoro-name"))
6499 |         XCTAssertTrue(record.contains(accepted))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6607:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6605 |         XCTAssertFalse(model.editorInputLocked)
6606 |         XCTAssertEqual(model.statusText, "Named DEEP WORK in 2026/20260828.md")
6607 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6608 |         XCTAssertTrue(
6609 |             record.contains(

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6834:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6832 |         await waitUntil { model.completionResponse?.context == "wikilink_note" }
6833 | 
6834 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6835 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 9 --format json -- prefix [[AI suffix"))
6836 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7107:28: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
7105 |         }
7106 | 
7107 |         let record = (try? String(contentsOf: recordURL)) ?? ""
     |                            `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
7108 |         return record.contains("argv=capture-parse --format json -- \(draft)")
7109 |             && record.contains("argv=capture --dry-run --no-clip --format json -- \(draft)")

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
PASS BobMacCaptureInstallHelperTests
PASS CaptureCoreTests
PASS RefsCoreTests
Type-check only: macOS test targets were checked against a stub; CI still runs the tests.
error: recipe `typecheck-tests` failed on line 30 with exit code 1
failed  exit=1  duration=242288ms

