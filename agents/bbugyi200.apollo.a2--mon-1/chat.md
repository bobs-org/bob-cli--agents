# Chat History - ace-run (a2--mon-1)

- **TIMESTAMP:** 2026-10-23 10:31:17 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** a2--mon-1

## Prompt

sase monitor start --command 'bash -o pipefail -c \'tar -C \'"\'"\'/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/linked/bob-mac-capture\'"\'"\' --exclude=.git --exclude=.build -cf - . | ssh -o BatchMode=yes mac \'"\'"\'set -e; scratch=$(mktemp -d /tmp/bob-mac-capture-check.XXXXXX); trap \'"\'"\'\\\'"\'"\'\'"\'"\'rm -rf "$scratch"\'"\'"\'\\\'"\'"\'\'"\'"\' EXIT; tar -xf - -C "$scratch"; cd "$scratch"; Scripts/bundle.sh; just typecheck-tests\'"\'"\'\'' --reason 'Compile the approved Bob Mac Capture changes on macOS from a streamed disposable copy'

## Response

sase: running unwrapped (no profile (monitor.tool_wrap is verify))
Building for production...
[0/6] Write sources
[3/6] Write swift-version--1AB21518FC5DEDBE.txt
[5/7] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[6/8] Compiling RefsCore RefsArrivals.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
376 | 
377 |   private let fileURL: URL
378 |   private let fileManager: FileManager
    |               `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
379 |   private let onError: @Sendable (String) -> Void
380 |   private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[7/9] Compiling BobMacCapture AccessibilityTrust.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
865 |     }
866 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
865 |     }
866 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:77:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 75 |     NSApplication.shared.addSceneRepresentation(representation)
 76 |     settingsSceneRepresentation = representation
 77 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 78 |       representation.environment.openSettings()
 79 |     }
    :
859 |   var activateApplication: () -> Void
860 | 
861 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:280:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
278 |     menu.addItem(redo)
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
282 |     menu.addItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:281:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     menu.addItem(
283 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:290:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
288 |     )
289 |     menu.addItem(
290 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     return menu
292 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:487:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
485 |   /// off MainActor state.
486 |   nonisolated static func storedHighlightsAppPath() -> String {
487 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
488 |   }
489 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:567:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
565 |       library: library,
566 |       opener: WorkspaceRefsOpener(),
567 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
568 |       tabs: tabsSession,
569 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:770:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
768 |       return
769 |     }
770 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
771 |   }
772 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:196:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
194 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
195 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
196 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
197 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
198 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8674:23: warning: no 'async' operations occur within 'await' expression
 8672 |                 }
 8673 | 
 8674 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8675 |                     return
 8676 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8679:21: warning: no 'async' operations occur within 'await' expression
 8677 | 
 8678 |                 if pickerNeeded == nil {
 8679 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8680 |                         draft: draft,
 8681 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8693:27: warning: no 'async' operations occur within 'await' expression
 8691 |                     await completionGate.value
 8692 |                     try Task.checkCancellation()
 8693 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8694 |                         return
 8695 |                     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8700:20: warning: no 'async' operations occur within 'await' expression
 8698 |                 if let cursorUTF8Offset,
 8699 |                    requestCompletion,
 8700 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8701 |                        parse: parse,
 8702 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8706:37: warning: no 'async' operations occur within 'await' expression
 8704 |                    ) == true
 8705 |                 {
 8706 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8707 |                         parse: parse,
 8708 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8935:28: warning: no 'async' operations occur within 'await' expression
 8933 |         Task { [weak self, processClient] in
 8934 |             do {
 8935 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 8936 |                 let processClientIdentity = processClient.identityToken
 8937 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
179 | @MainActor
180 | public final class RefsDecodedImageBudget {
181 |   public static let defaultByteLimit = RefsAnnotationImageLoader.bitmapCacheByteLimit
    |                     `- note: static property declared here
182 | 
183 |   private let byteLimit: Int
    :
186 |   public private(set) var byteCost = 0
187 | 
188 |   public init(byteLimit: Int = defaultByteLimit) {
    |                                `- warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
189 |     self.byteLimit = max(byteLimit, 1)
190 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:628:14: warning: no 'async' operations occur within 'await' expression
 626 |     }.store(in: &subscriptions)
 627 |     library.$scanState.sink { [weak self] _ in
 628 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:631:14: warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in
 631 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 632 |     }.store(in: &subscriptions)
 633 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2992:7: warning: result of call to 'openSelected' is unused [#no-usage]
2990 |       openWithDefaultApp(item)
2991 |     case .note, .reveal:
2992 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2993 |     }
2994 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3024:9: warning: no 'async' operations occur within 'await' expression
3022 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3023 |       Task {
3024 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3025 |       }
3026 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3051:9: warning: no 'async' operations occur within 'await' expression
3049 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3050 |       Task {
3051 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3052 |       }
3053 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3109:9: warning: no 'async' operations occur within 'await' expression
3107 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3108 |       Task {
3109 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3110 |           itemID: item.id,
3111 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3140:9: warning: no 'async' operations occur within 'await' expression
3138 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3139 |       Task {
3140 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3141 |           itemID: item.id,
3142 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
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
[7/9] Write Objects.LinkFileList
[8/9] Linking BobMacCapture
Build of product 'BobMacCapture' complete! (181.19s)
/tmp/bob-mac-capture-check.gpWDb2/.build/bundle/Bob Mac Capture.app/Contents/MacOS/BobMacCapture: replacing existing signature
/tmp/bob-mac-capture-check.gpWDb2/.build/bundle/Bob Mac Capture.app: replacing existing signature
/tmp/bob-mac-capture-check.gpWDb2/.build/bundle/Bob Mac Capture.app
./Scripts/typecheck-tests.sh
Building for debugging...
[0/18] Write sources
[5/18] Write BobMacCaptureInstallHelper-entitlement.plist
[5/18] Write refs-rank-entitlement.plist
[7/18] Write BobMacCapture-entitlement.plist
[8/18] Write swift-version--1AB21518FC5DEDBE.txt
[10/77] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[11/77] Compiling CaptureCore BlockIDPickerIndex.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[12/77] Compiling CaptureCore BlockIDRules.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[13/77] Compiling CaptureCore BobEnvironment.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[14/77] Compiling CaptureCore BobErrors.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[15/77] Compiling CaptureCore BobExecutableResolver.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[16/77] Compiling CaptureCore BobMacCaptureLaunchContext.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[17/77] Compiling CaptureCore BobProcessClient.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[18/77] Compiling CaptureCore CanceledDraftStashStore.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[19/77] Compiling CaptureCore CapturePomodoroLinkPresentation.swift
[20/77] Compiling CaptureCore CapturePomodoroResetPresentation.swift
[21/77] Compiling CaptureCore CapturePomodoroShiftPresentation.swift
[22/77] Compiling CaptureCore CapturePomodoroStartPresentation.swift
[23/77] Compiling CaptureCore CaptureProjectNotePresentation.swift
[24/77] Compiling CaptureCore CaptureRefFileUnder.swift
[25/77] Compiling CaptureCore CaptureRefPresentation.swift
[26/77] Compiling CaptureCore CaptureRelatedModels.swift
[27/77] Compiling CaptureCore CapturePanelPlacement.swift
[28/77] Compiling CaptureCore CapturePickerHelpers.swift
[29/77] Compiling CaptureCore CapturePickerPresentation.swift
[30/77] Compiling CaptureCore CapturePlanBudgetPresentation.swift
[31/77] Compiling CaptureCore CapturePomodoroAdjustPresentation.swift
[32/77] Compiling CaptureCore CapturePomodoroBlockPresentation.swift
[33/77] Compiling CaptureCore CapturePomodoroClosePresentation.swift
[34/77] Compiling CaptureCore CapturePomodoroLineTokens.swift
[35/77] Compiling CaptureCore CaptureAgendaFitPlanner.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[36/77] Compiling CaptureCore CaptureAgendaHold.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[37/77] Compiling CaptureCore CaptureAgendaInlineText.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[38/77] Compiling CaptureCore CaptureAgendaLayout.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[39/77] Compiling CaptureCore CaptureAgendaModels.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[40/77] Compiling CaptureCore CaptureAgendaPresentation.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[41/77] Compiling CaptureCore CaptureAgendaRefreshFilter.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[42/77] Compiling CaptureCore CaptureAgendaRefreshState.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[43/77] Compiling CaptureCore CaptureAgendaVisibility.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[44/77] Compiling CaptureCore CaptureRelationshipCopy.swift
[45/77] Compiling CaptureCore CaptureRelationshipPresentation.swift
[46/77] Compiling CaptureCore CaptureSavedTemplates.swift
[47/77] Compiling CaptureCore CaptureSubBulletPresentation.swift
[48/77] Compiling CaptureCore CaptureSuccessorPresentation.swift
[49/77] Compiling CaptureCore CaptureTargetsCache.swift
[50/77] Compiling CaptureCore CaptureTaskBlockPresentation.swift
[51/77] Compiling CaptureCore CaptureTaskCompletePresentation.swift
[52/77] Compiling CaptureCore CaptureTemplateStart.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[53/77] Compiling CaptureCore CaptureTextRanges.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[54/77] Compiling CaptureCore CaptureTodayPomodoroGoto.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[55/77] Compiling CaptureCore CaptureTogglePresentation.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[56/77] Compiling CaptureCore CompletionRowContent.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[57/77] Compiling CaptureCore DependencyPickerPresentation.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[58/77] Compiling CaptureCore FuzzyMatcher.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[59/77] Compiling CaptureCore ObsidianOpenURL.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[60/85] Compiling CaptureCore ParentTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[61/85] Compiling CaptureCore PomodoroHomes.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[62/85] Compiling CaptureCore SimilarTasksBandEdits.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[63/85] Compiling CaptureCore SimilarTasksBandPolicy.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[64/85] Compiling CaptureCore SimilarTasksBandPresentation.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[65/85] Compiling CaptureCore TaskCompletePickerPresentation.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[66/85] Compiling CaptureCore TaskDisplayText.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[67/85] Compiling CaptureCore TaskLinkPickerPresentation.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[68/85] Compiling CaptureCore CaptureBlockDiffRow.swift
[69/85] Compiling CaptureCore CaptureCloseTaskCommaAssist.swift
[70/85] Compiling CaptureCore CaptureCloseTaskCommaProvenance.swift
[71/85] Compiling CaptureCore CaptureEditWrite.swift
[72/85] Compiling CaptureCore CaptureLinkGuardPresentation.swift
[73/85] Compiling CaptureCore CaptureModels.swift
[74/85] Compiling CaptureCore CaptureOpenHintPresentation.swift
[75/85] Compiling CaptureCore CaptureOpenPlan.swift
[76/85] Emitting module CaptureCore
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[77/115] Emitting module RefsCore
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
376 | 
377 |   private let fileURL: URL
378 |   private let fileManager: FileManager
    |               `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
379 |   private let onError: @Sendable (String) -> Void
380 |   private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[78/118] Compiling RefsCore RefsNewest.swift
[79/118] Compiling RefsCore RefsPanelGeometry.swift
[80/118] Compiling RefsCore RefsQuoteUnderline.swift
[81/118] Compiling RefsCore RefsInspectorImages.swift
[82/118] Compiling RefsCore RefsListScroll.swift
[83/118] Compiling RefsCore RefsModel.swift
[84/118] Compiling RefsCore RefsNew.swift
[85/118] Compiling RefsCore RefsSelection.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
376 | 
377 |   private let fileURL: URL
378 |   private let fileManager: FileManager
    |               `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
379 |   private let onError: @Sendable (String) -> Void
380 |   private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[86/118] Compiling RefsCore RefsStores.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
376 | 
377 |   private let fileURL: URL
378 |   private let fileManager: FileManager
    |               `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
379 |   private let onError: @Sendable (String) -> Void
380 |   private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[87/118] Compiling RefsCore RefsTabClose.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
376 | 
377 |   private let fileURL: URL
378 |   private let fileManager: FileManager
    |               `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
379 |   private let onError: @Sendable (String) -> Void
380 |   private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[88/118] Compiling RefsCore RefsTabsRanking.swift
[89/118] Compiling RefsCore RefsToday.swift
[90/118] Compiling RefsCore RefsTodayLinkCard.swift
[91/118] Compiling RefsCore RefsTodayLinkModels.swift
[92/118] Compiling RefsCore RefsTodayLinkPresentation.swift
[93/118] Compiling RefsCore RefsWatcherRelevance.swift
[94/118] Compiling RefsCore RefsFetching.swift
[95/118] Compiling RefsCore RefsHighlightPicker.swift
[96/118] Compiling RefsCore RefsHighlightsTabs.swift
[97/118] Compiling RefsCore RefsInspector.swift
[98/118] Compiling RefsCore RefsArrivals.swift
[99/118] Compiling RefsCore RefsCaption.swift
[100/118] Compiling RefsCore RefsCopy.swift
[101/118] Compiling RefsCore RefsDecoding.swift
[102/118] Compiling RefsCore RefsRanking.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {
[103/118] Compiling RefsCore RefsRename.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {
[104/118] Compiling RefsCore RefsScan.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {
[105/184] Compiling refs_rank main.swift
[106/184] Emitting module refs_rank
[106/184] Write Objects.LinkFileList
[107/184] Linking refs-rank
[108/184] Applying refs-rank
[110/184] Compiling BobMacCaptureInstallHelper InstallHelperArguments.swift
[111/184] Compiling BobMacCaptureInstallHelper InstallHelperError.swift
[112/184] Compiling BobMacCaptureInstallHelper InstallRelauncher.swift
[113/184] Emitting module BobMacCaptureInstallHelper
[114/184] Compiling BobMacCaptureInstallHelper BobMacCaptureInstallHelperMain.swift
[114/184] Write Objects.LinkFileList
[115/184] Linking BobMacCaptureInstallHelper
[116/184] Applying BobMacCaptureInstallHelper
[118/184] Compiling BobMacCapture CaptureSnippetResolver.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.
[119/184] Compiling BobMacCapture CaptureTargetsRefreshGate.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.
[120/184] Compiling BobMacCapture HighlightsTakeover.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.
[121/184] Compiling BobMacCapture HotKeyRegistry.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.
[122/184] Compiling BobMacCapture NotificationService.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.
[123/184] Compiling BobMacCapture PlainTextPaste.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.
[124/184] Compiling BobMacCapture PomodoroBlockView.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.
[125/184] Compiling BobMacCapture PomodoroHomeColor.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.
[126/184] Compiling BobMacCapture PomodoroNameField.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.
[127/193] Compiling BobMacCapture AccessibilityTrust.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
865 |     }
866 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
865 |     }
866 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:77:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 75 |     NSApplication.shared.addSceneRepresentation(representation)
 76 |     settingsSceneRepresentation = representation
 77 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 78 |       representation.environment.openSettings()
 79 |     }
    :
859 |   var activateApplication: () -> Void
860 | 
861 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:280:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
278 |     menu.addItem(redo)
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
282 |     menu.addItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:281:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     menu.addItem(
283 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:290:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
288 |     )
289 |     menu.addItem(
290 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     return menu
292 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:487:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
485 |   /// off MainActor state.
486 |   nonisolated static func storedHighlightsAppPath() -> String {
487 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
488 |   }
489 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:567:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
565 |       library: library,
566 |       opener: WorkspaceRefsOpener(),
567 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
568 |       tabs: tabsSession,
569 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:770:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
768 |       return
769 |     }
770 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
771 |   }
772 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:196:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
194 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
195 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
196 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
197 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
198 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[128/193] Compiling BobMacCapture AppDelegate.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
865 |     }
866 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
865 |     }
866 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:77:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 75 |     NSApplication.shared.addSceneRepresentation(representation)
 76 |     settingsSceneRepresentation = representation
 77 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 78 |       representation.environment.openSettings()
 79 |     }
    :
859 |   var activateApplication: () -> Void
860 | 
861 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:280:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
278 |     menu.addItem(redo)
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
282 |     menu.addItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:281:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     menu.addItem(
283 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:290:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
288 |     )
289 |     menu.addItem(
290 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     return menu
292 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:487:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
485 |   /// off MainActor state.
486 |   nonisolated static func storedHighlightsAppPath() -> String {
487 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
488 |   }
489 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:567:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
565 |       library: library,
566 |       opener: WorkspaceRefsOpener(),
567 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
568 |       tabs: tabsSession,
569 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:770:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
768 |       return
769 |     }
770 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
771 |   }
772 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:196:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
194 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
195 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
196 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
197 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
198 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[129/193] Compiling BobMacCapture AppRelauncher.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
865 |     }
866 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
865 |     }
866 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:77:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 75 |     NSApplication.shared.addSceneRepresentation(representation)
 76 |     settingsSceneRepresentation = representation
 77 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 78 |       representation.environment.openSettings()
 79 |     }
    :
859 |   var activateApplication: () -> Void
860 | 
861 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:280:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
278 |     menu.addItem(redo)
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
282 |     menu.addItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:281:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     menu.addItem(
283 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:290:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
288 |     )
289 |     menu.addItem(
290 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     return menu
292 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:487:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
485 |   /// off MainActor state.
486 |   nonisolated static func storedHighlightsAppPath() -> String {
487 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
488 |   }
489 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:567:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
565 |       library: library,
566 |       opener: WorkspaceRefsOpener(),
567 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
568 |       tabs: tabsSession,
569 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:770:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
768 |       return
769 |     }
770 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
771 |   }
772 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:196:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
194 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
195 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
196 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
197 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
198 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[130/193] Compiling BobMacCapture AppSettings.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
865 |     }
866 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
865 |     }
866 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:77:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 75 |     NSApplication.shared.addSceneRepresentation(representation)
 76 |     settingsSceneRepresentation = representation
 77 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 78 |       representation.environment.openSettings()
 79 |     }
    :
859 |   var activateApplication: () -> Void
860 | 
861 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:280:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
278 |     menu.addItem(redo)
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
282 |     menu.addItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:281:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     menu.addItem(
283 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:290:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
288 |     )
289 |     menu.addItem(
290 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     return menu
292 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:487:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
485 |   /// off MainActor state.
486 |   nonisolated static func storedHighlightsAppPath() -> String {
487 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
488 |   }
489 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:567:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
565 |       library: library,
566 |       opener: WorkspaceRefsOpener(),
567 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
568 |       tabs: tabsSession,
569 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:770:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
768 |       return
769 |     }
770 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
771 |   }
772 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:196:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
194 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
195 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
196 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
197 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
198 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[131/193] Compiling BobMacCapture BlockDiffCard.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
865 |     }
866 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
865 |     }
866 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:77:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 75 |     NSApplication.shared.addSceneRepresentation(representation)
 76 |     settingsSceneRepresentation = representation
 77 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 78 |       representation.environment.openSettings()
 79 |     }
    :
859 |   var activateApplication: () -> Void
860 | 
861 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:280:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
278 |     menu.addItem(redo)
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
282 |     menu.addItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:281:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     menu.addItem(
283 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:290:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
288 |     )
289 |     menu.addItem(
290 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     return menu
292 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:487:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
485 |   /// off MainActor state.
486 |   nonisolated static func storedHighlightsAppPath() -> String {
487 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
488 |   }
489 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:567:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
565 |       library: library,
566 |       opener: WorkspaceRefsOpener(),
567 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
568 |       tabs: tabsSession,
569 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:770:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
768 |       return
769 |     }
770 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
771 |   }
772 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:196:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
194 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
195 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
196 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
197 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
198 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[132/193] Compiling BobMacCapture BlockIDField.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
865 |     }
866 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
865 |     }
866 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:77:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 75 |     NSApplication.shared.addSceneRepresentation(representation)
 76 |     settingsSceneRepresentation = representation
 77 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 78 |       representation.environment.openSettings()
 79 |     }
    :
859 |   var activateApplication: () -> Void
860 | 
861 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:280:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
278 |     menu.addItem(redo)
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
282 |     menu.addItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:281:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     menu.addItem(
283 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:290:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
288 |     )
289 |     menu.addItem(
290 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     return menu
292 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:487:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
485 |   /// off MainActor state.
486 |   nonisolated static func storedHighlightsAppPath() -> String {
487 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
488 |   }
489 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:567:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
565 |       library: library,
566 |       opener: WorkspaceRefsOpener(),
567 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
568 |       tabs: tabsSession,
569 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:770:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
768 |       return
769 |     }
770 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
771 |   }
772 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:196:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
194 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
195 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
196 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
197 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
198 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[133/193] Compiling BobMacCapture BobMacCaptureMain.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
865 |     }
866 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
865 |     }
866 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:77:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 75 |     NSApplication.shared.addSceneRepresentation(representation)
 76 |     settingsSceneRepresentation = representation
 77 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 78 |       representation.environment.openSettings()
 79 |     }
    :
859 |   var activateApplication: () -> Void
860 | 
861 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:280:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
278 |     menu.addItem(redo)
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
282 |     menu.addItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:281:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     menu.addItem(
283 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:290:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
288 |     )
289 |     menu.addItem(
290 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     return menu
292 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:487:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
485 |   /// off MainActor state.
486 |   nonisolated static func storedHighlightsAppPath() -> String {
487 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
488 |   }
489 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:567:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
565 |       library: library,
566 |       opener: WorkspaceRefsOpener(),
567 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
568 |       tabs: tabsSession,
569 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:770:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
768 |       return
769 |     }
770 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
771 |   }
772 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:196:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
194 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
195 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
196 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
197 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
198 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[134/193] Compiling BobMacCapture BobPanelCoordinator.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
865 |     }
866 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
865 |     }
866 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:77:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 75 |     NSApplication.shared.addSceneRepresentation(representation)
 76 |     settingsSceneRepresentation = representation
 77 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 78 |       representation.environment.openSettings()
 79 |     }
    :
859 |   var activateApplication: () -> Void
860 | 
861 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:280:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
278 |     menu.addItem(redo)
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
282 |     menu.addItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:281:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     menu.addItem(
283 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:290:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
288 |     )
289 |     menu.addItem(
290 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     return menu
292 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:487:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
485 |   /// off MainActor state.
486 |   nonisolated static func storedHighlightsAppPath() -> String {
487 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
488 |   }
489 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:567:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
565 |       library: library,
566 |       opener: WorkspaceRefsOpener(),
567 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
568 |       tabs: tabsSession,
569 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:770:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
768 |       return
769 |     }
770 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
771 |   }
772 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:196:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
194 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
195 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
196 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
197 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
198 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[135/193] Compiling BobMacCapture BundleSigningInspector.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
865 |     }
866 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
865 |     }
866 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:77:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 75 |     NSApplication.shared.addSceneRepresentation(representation)
 76 |     settingsSceneRepresentation = representation
 77 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 78 |       representation.environment.openSettings()
 79 |     }
    :
859 |   var activateApplication: () -> Void
860 | 
861 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:280:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
278 |     menu.addItem(redo)
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
282 |     menu.addItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:281:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     menu.addItem(.separator())
280 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
281 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     menu.addItem(
283 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:290:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
288 |     )
289 |     menu.addItem(
290 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     return menu
292 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:487:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
485 |   /// off MainActor state.
486 |   nonisolated static func storedHighlightsAppPath() -> String {
487 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
488 |   }
489 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:567:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
565 |       library: library,
566 |       opener: WorkspaceRefsOpener(),
567 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
568 |       tabs: tabsSession,
569 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:770:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
768 |       return
769 |     }
770 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
771 |   }
772 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:196:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
194 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
195 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
196 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
197 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
198 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[136/193] Compiling BobMacCapture RefsRenameCardView.swift
[137/193] Compiling BobMacCapture RefsRowView.swift
[138/193] Compiling BobMacCapture RefsSearchBar.swift
[139/193] Compiling BobMacCapture RefsTabsViews.swift
[140/193] Compiling BobMacCapture RefsTodayLinkCardView.swift
[141/193] Compiling BobMacCapture RefsUnderlineRenderer.swift
[142/193] Compiling BobMacCapture RefsVisualTokens.swift
[143/193] Compiling BobMacCapture RefsHighlightsOpenKey.swift
[144/193] Compiling BobMacCapture RefsHighlightsTabsKey.swift
[145/193] Compiling BobMacCapture RefsHotkeyRegistration.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[146/193] Compiling BobMacCapture SavedTemplateShelf.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[147/193] Compiling BobMacCapture SettingsView.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[148/193] Compiling BobMacCapture Signposts.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[149/193] Compiling BobMacCapture SimilarTasksBandView.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[150/193] Compiling BobMacCapture StatusItemController.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[151/193] Compiling BobMacCapture StatusItemGlyph.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[152/193] Compiling BobMacCapture TaskBlockView.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[153/193] Compiling BobMacCapture VaultTargetWatcher.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[154/193] Compiling BobMacCapture CanceledDraftStash.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8674:23: warning: no 'async' operations occur within 'await' expression
 8672 |                 }
 8673 | 
 8674 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8675 |                     return
 8676 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8679:21: warning: no 'async' operations occur within 'await' expression
 8677 | 
 8678 |                 if pickerNeeded == nil {
 8679 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8680 |                         draft: draft,
 8681 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8693:27: warning: no 'async' operations occur within 'await' expression
 8691 |                     await completionGate.value
 8692 |                     try Task.checkCancellation()
 8693 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8694 |                         return
 8695 |                     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8700:20: warning: no 'async' operations occur within 'await' expression
 8698 |                 if let cursorUTF8Offset,
 8699 |                    requestCompletion,
 8700 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8701 |                        parse: parse,
 8702 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8706:37: warning: no 'async' operations occur within 'await' expression
 8704 |                    ) == true
 8705 |                 {
 8706 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8707 |                         parse: parse,
 8708 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8935:28: warning: no 'async' operations occur within 'await' expression
 8933 |         Task { [weak self, processClient] in
 8934 |             do {
 8935 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 8936 |                 let processClientIdentity = processClient.identityToken
 8937 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[155/193] Compiling BobMacCapture CaptureAgendaRowMeasurer.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8674:23: warning: no 'async' operations occur within 'await' expression
 8672 |                 }
 8673 | 
 8674 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8675 |                     return
 8676 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8679:21: warning: no 'async' operations occur within 'await' expression
 8677 | 
 8678 |                 if pickerNeeded == nil {
 8679 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8680 |                         draft: draft,
 8681 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8693:27: warning: no 'async' operations occur within 'await' expression
 8691 |                     await completionGate.value
 8692 |                     try Task.checkCancellation()
 8693 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8694 |                         return
 8695 |                     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8700:20: warning: no 'async' operations occur within 'await' expression
 8698 |                 if let cursorUTF8Offset,
 8699 |                    requestCompletion,
 8700 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8701 |                        parse: parse,
 8702 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8706:37: warning: no 'async' operations occur within 'await' expression
 8704 |                    ) == true
 8705 |                 {
 8706 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8707 |                         parse: parse,
 8708 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8935:28: warning: no 'async' operations occur within 'await' expression
 8933 |         Task { [weak self, processClient] in
 8934 |             do {
 8935 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 8936 |                 let processClientIdentity = processClient.identityToken
 8937 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[156/193] Compiling BobMacCapture CaptureAgendaStore.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8674:23: warning: no 'async' operations occur within 'await' expression
 8672 |                 }
 8673 | 
 8674 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8675 |                     return
 8676 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8679:21: warning: no 'async' operations occur within 'await' expression
 8677 | 
 8678 |                 if pickerNeeded == nil {
 8679 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8680 |                         draft: draft,
 8681 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8693:27: warning: no 'async' operations occur within 'await' expression
 8691 |                     await completionGate.value
 8692 |                     try Task.checkCancellation()
 8693 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8694 |                         return
 8695 |                     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8700:20: warning: no 'async' operations occur within 'await' expression
 8698 |                 if let cursorUTF8Offset,
 8699 |                    requestCompletion,
 8700 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8701 |                        parse: parse,
 8702 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8706:37: warning: no 'async' operations occur within 'await' expression
 8704 |                    ) == true
 8705 |                 {
 8706 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8707 |                         parse: parse,
 8708 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8935:28: warning: no 'async' operations occur within 'await' expression
 8933 |         Task { [weak self, processClient] in
 8934 |             do {
 8935 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 8936 |                 let processClientIdentity = processClient.identityToken
 8937 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[157/193] Compiling BobMacCapture CaptureAgendaView.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8674:23: warning: no 'async' operations occur within 'await' expression
 8672 |                 }
 8673 | 
 8674 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8675 |                     return
 8676 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8679:21: warning: no 'async' operations occur within 'await' expression
 8677 | 
 8678 |                 if pickerNeeded == nil {
 8679 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8680 |                         draft: draft,
 8681 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8693:27: warning: no 'async' operations occur within 'await' expression
 8691 |                     await completionGate.value
 8692 |                     try Task.checkCancellation()
 8693 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8694 |                         return
 8695 |                     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8700:20: warning: no 'async' operations occur within 'await' expression
 8698 |                 if let cursorUTF8Offset,
 8699 |                    requestCompletion,
 8700 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8701 |                        parse: parse,
 8702 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8706:37: warning: no 'async' operations occur within 'await' expression
 8704 |                    ) == true
 8705 |                 {
 8706 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8707 |                         parse: parse,
 8708 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8935:28: warning: no 'async' operations occur within 'await' expression
 8933 |         Task { [weak self, processClient] in
 8934 |             do {
 8935 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 8936 |                 let processClientIdentity = processClient.identityToken
 8937 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[158/193] Compiling BobMacCapture CaptureEditorPalette.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8674:23: warning: no 'async' operations occur within 'await' expression
 8672 |                 }
 8673 | 
 8674 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8675 |                     return
 8676 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8679:21: warning: no 'async' operations occur within 'await' expression
 8677 | 
 8678 |                 if pickerNeeded == nil {
 8679 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8680 |                         draft: draft,
 8681 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8693:27: warning: no 'async' operations occur within 'await' expression
 8691 |                     await completionGate.value
 8692 |                     try Task.checkCancellation()
 8693 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8694 |                         return
 8695 |                     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8700:20: warning: no 'async' operations occur within 'await' expression
 8698 |                 if let cursorUTF8Offset,
 8699 |                    requestCompletion,
 8700 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8701 |                        parse: parse,
 8702 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8706:37: warning: no 'async' operations occur within 'await' expression
 8704 |                    ) == true
 8705 |                 {
 8706 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8707 |                         parse: parse,
 8708 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8935:28: warning: no 'async' operations occur within 'await' expression
 8933 |         Task { [weak self, processClient] in
 8934 |             do {
 8935 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 8936 |                 let processClientIdentity = processClient.identityToken
 8937 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[159/193] Compiling BobMacCapture CaptureEditorTextConfiguration.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8674:23: warning: no 'async' operations occur within 'await' expression
 8672 |                 }
 8673 | 
 8674 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8675 |                     return
 8676 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8679:21: warning: no 'async' operations occur within 'await' expression
 8677 | 
 8678 |                 if pickerNeeded == nil {
 8679 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8680 |                         draft: draft,
 8681 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8693:27: warning: no 'async' operations occur within 'await' expression
 8691 |                     await completionGate.value
 8692 |                     try Task.checkCancellation()
 8693 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8694 |                         return
 8695 |                     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8700:20: warning: no 'async' operations occur within 'await' expression
 8698 |                 if let cursorUTF8Offset,
 8699 |                    requestCompletion,
 8700 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8701 |                        parse: parse,
 8702 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8706:37: warning: no 'async' operations occur within 'await' expression
 8704 |                    ) == true
 8705 |                 {
 8706 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8707 |                         parse: parse,
 8708 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8935:28: warning: no 'async' operations occur within 'await' expression
 8933 |         Task { [weak self, processClient] in
 8934 |             do {
 8935 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 8936 |                 let processClientIdentity = processClient.identityToken
 8937 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[160/193] Compiling BobMacCapture CaptureKeyCommandRouter.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8674:23: warning: no 'async' operations occur within 'await' expression
 8672 |                 }
 8673 | 
 8674 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8675 |                     return
 8676 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8679:21: warning: no 'async' operations occur within 'await' expression
 8677 | 
 8678 |                 if pickerNeeded == nil {
 8679 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8680 |                         draft: draft,
 8681 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8693:27: warning: no 'async' operations occur within 'await' expression
 8691 |                     await completionGate.value
 8692 |                     try Task.checkCancellation()
 8693 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8694 |                         return
 8695 |                     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8700:20: warning: no 'async' operations occur within 'await' expression
 8698 |                 if let cursorUTF8Offset,
 8699 |                    requestCompletion,
 8700 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8701 |                        parse: parse,
 8702 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8706:37: warning: no 'async' operations occur within 'await' expression
 8704 |                    ) == true
 8705 |                 {
 8706 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8707 |                         parse: parse,
 8708 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8935:28: warning: no 'async' operations occur within 'await' expression
 8933 |         Task { [weak self, processClient] in
 8934 |             do {
 8935 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 8936 |                 let processClientIdentity = processClient.identityToken
 8937 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[161/193] Compiling BobMacCapture CapturePanelController.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8674:23: warning: no 'async' operations occur within 'await' expression
 8672 |                 }
 8673 | 
 8674 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8675 |                     return
 8676 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8679:21: warning: no 'async' operations occur within 'await' expression
 8677 | 
 8678 |                 if pickerNeeded == nil {
 8679 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8680 |                         draft: draft,
 8681 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8693:27: warning: no 'async' operations occur within 'await' expression
 8691 |                     await completionGate.value
 8692 |                     try Task.checkCancellation()
 8693 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8694 |                         return
 8695 |                     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8700:20: warning: no 'async' operations occur within 'await' expression
 8698 |                 if let cursorUTF8Offset,
 8699 |                    requestCompletion,
 8700 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8701 |                        parse: parse,
 8702 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8706:37: warning: no 'async' operations occur within 'await' expression
 8704 |                    ) == true
 8705 |                 {
 8706 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8707 |                         parse: parse,
 8708 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8935:28: warning: no 'async' operations occur within 'await' expression
 8933 |         Task { [weak self, processClient] in
 8934 |             do {
 8935 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 8936 |                 let processClientIdentity = processClient.identityToken
 8937 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[162/193] Compiling BobMacCapture CapturePanelModel.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:2027:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2025 |                         refuseOverride: !allowsOverride,
 2026 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2027 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2028 |                     )
 2029 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8674:23: warning: no 'async' operations occur within 'await' expression
 8672 |                 }
 8673 | 
 8674 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8675 |                     return
 8676 |                 }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8679:21: warning: no 'async' operations occur within 'await' expression
 8677 | 
 8678 |                 if pickerNeeded == nil {
 8679 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8680 |                         draft: draft,
 8681 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8693:27: warning: no 'async' operations occur within 'await' expression
 8691 |                     await completionGate.value
 8692 |                     try Task.checkCancellation()
 8693 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8694 |                         return
 8695 |                     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8700:20: warning: no 'async' operations occur within 'await' expression
 8698 |                 if let cursorUTF8Offset,
 8699 |                    requestCompletion,
 8700 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8701 |                        parse: parse,
 8702 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8706:37: warning: no 'async' operations occur within 'await' expression
 8704 |                    ) == true
 8705 |                 {
 8706 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8707 |                         parse: parse,
 8708 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePanelModel.swift:8935:28: warning: no 'async' operations occur within 'await' expression
 8933 |         Task { [weak self, processClient] in
 8934 |             do {
 8935 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 8936 |                 let processClientIdentity = processClient.identityToken
 8937 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[163/193] Compiling BobMacCapture RefsInspectorView.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:628:14: warning: no 'async' operations occur within 'await' expression
 626 |     }.store(in: &subscriptions)
 627 |     library.$scanState.sink { [weak self] _ in
 628 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:631:14: warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in
 631 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 632 |     }.store(in: &subscriptions)
 633 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2992:7: warning: result of call to 'openSelected' is unused [#no-usage]
2990 |       openWithDefaultApp(item)
2991 |     case .note, .reveal:
2992 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2993 |     }
2994 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3024:9: warning: no 'async' operations occur within 'await' expression
3022 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3023 |       Task {
3024 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3025 |       }
3026 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3051:9: warning: no 'async' operations occur within 'await' expression
3049 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3050 |       Task {
3051 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3052 |       }
3053 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3109:9: warning: no 'async' operations occur within 'await' expression
3107 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3108 |       Task {
3109 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3110 |           itemID: item.id,
3111 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3140:9: warning: no 'async' operations occur within 'await' expression
3138 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3139 |       Task {
3140 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3141 |           itemID: item.id,
3142 |           title: item.title.text,
[164/193] Compiling BobMacCapture RefsKeyRouter.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:628:14: warning: no 'async' operations occur within 'await' expression
 626 |     }.store(in: &subscriptions)
 627 |     library.$scanState.sink { [weak self] _ in
 628 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:631:14: warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in
 631 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 632 |     }.store(in: &subscriptions)
 633 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2992:7: warning: result of call to 'openSelected' is unused [#no-usage]
2990 |       openWithDefaultApp(item)
2991 |     case .note, .reveal:
2992 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2993 |     }
2994 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3024:9: warning: no 'async' operations occur within 'await' expression
3022 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3023 |       Task {
3024 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3025 |       }
3026 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3051:9: warning: no 'async' operations occur within 'await' expression
3049 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3050 |       Task {
3051 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3052 |       }
3053 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3109:9: warning: no 'async' operations occur within 'await' expression
3107 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3108 |       Task {
3109 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3110 |           itemID: item.id,
3111 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3140:9: warning: no 'async' operations occur within 'await' expression
3138 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3139 |       Task {
3140 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3141 |           itemID: item.id,
3142 |           title: item.title.text,
[165/193] Compiling BobMacCapture RefsLibrary.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:628:14: warning: no 'async' operations occur within 'await' expression
 626 |     }.store(in: &subscriptions)
 627 |     library.$scanState.sink { [weak self] _ in
 628 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:631:14: warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in
 631 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 632 |     }.store(in: &subscriptions)
 633 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2992:7: warning: result of call to 'openSelected' is unused [#no-usage]
2990 |       openWithDefaultApp(item)
2991 |     case .note, .reveal:
2992 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2993 |     }
2994 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3024:9: warning: no 'async' operations occur within 'await' expression
3022 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3023 |       Task {
3024 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3025 |       }
3026 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3051:9: warning: no 'async' operations occur within 'await' expression
3049 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3050 |       Task {
3051 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3052 |       }
3053 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3109:9: warning: no 'async' operations occur within 'await' expression
3107 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3108 |       Task {
3109 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3110 |           itemID: item.id,
3111 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3140:9: warning: no 'async' operations occur within 'await' expression
3138 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3139 |       Task {
3140 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3141 |           itemID: item.id,
3142 |           title: item.title.text,
[166/193] Compiling BobMacCapture RefsListView.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:628:14: warning: no 'async' operations occur within 'await' expression
 626 |     }.store(in: &subscriptions)
 627 |     library.$scanState.sink { [weak self] _ in
 628 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:631:14: warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in
 631 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 632 |     }.store(in: &subscriptions)
 633 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2992:7: warning: result of call to 'openSelected' is unused [#no-usage]
2990 |       openWithDefaultApp(item)
2991 |     case .note, .reveal:
2992 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2993 |     }
2994 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3024:9: warning: no 'async' operations occur within 'await' expression
3022 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3023 |       Task {
3024 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3025 |       }
3026 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3051:9: warning: no 'async' operations occur within 'await' expression
3049 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3050 |       Task {
3051 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3052 |       }
3053 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3109:9: warning: no 'async' operations occur within 'await' expression
3107 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3108 |       Task {
3109 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3110 |           itemID: item.id,
3111 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3140:9: warning: no 'async' operations occur within 'await' expression
3138 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3139 |       Task {
3140 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3141 |           itemID: item.id,
3142 |           title: item.title.text,
[167/193] Compiling BobMacCapture RefsPanel.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:628:14: warning: no 'async' operations occur within 'await' expression
 626 |     }.store(in: &subscriptions)
 627 |     library.$scanState.sink { [weak self] _ in
 628 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:631:14: warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in
 631 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 632 |     }.store(in: &subscriptions)
 633 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2992:7: warning: result of call to 'openSelected' is unused [#no-usage]
2990 |       openWithDefaultApp(item)
2991 |     case .note, .reveal:
2992 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2993 |     }
2994 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3024:9: warning: no 'async' operations occur within 'await' expression
3022 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3023 |       Task {
3024 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3025 |       }
3026 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3051:9: warning: no 'async' operations occur within 'await' expression
3049 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3050 |       Task {
3051 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3052 |       }
3053 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3109:9: warning: no 'async' operations occur within 'await' expression
3107 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3108 |       Task {
3109 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3110 |           itemID: item.id,
3111 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3140:9: warning: no 'async' operations occur within 'await' expression
3138 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3139 |       Task {
3140 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3141 |           itemID: item.id,
3142 |           title: item.title.text,
[168/193] Compiling BobMacCapture RefsPanelModel.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:628:14: warning: no 'async' operations occur within 'await' expression
 626 |     }.store(in: &subscriptions)
 627 |     library.$scanState.sink { [weak self] _ in
 628 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:631:14: warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in
 631 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 632 |     }.store(in: &subscriptions)
 633 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2992:7: warning: result of call to 'openSelected' is unused [#no-usage]
2990 |       openWithDefaultApp(item)
2991 |     case .note, .reveal:
2992 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2993 |     }
2994 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3024:9: warning: no 'async' operations occur within 'await' expression
3022 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3023 |       Task {
3024 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3025 |       }
3026 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3051:9: warning: no 'async' operations occur within 'await' expression
3049 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3050 |       Task {
3051 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3052 |       }
3053 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3109:9: warning: no 'async' operations occur within 'await' expression
3107 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3108 |       Task {
3109 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3110 |           itemID: item.id,
3111 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3140:9: warning: no 'async' operations occur within 'await' expression
3138 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3139 |       Task {
3140 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3141 |           itemID: item.id,
3142 |           title: item.title.text,
[169/193] Compiling BobMacCapture RefsPanelStates.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:628:14: warning: no 'async' operations occur within 'await' expression
 626 |     }.store(in: &subscriptions)
 627 |     library.$scanState.sink { [weak self] _ in
 628 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:631:14: warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in
 631 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 632 |     }.store(in: &subscriptions)
 633 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2992:7: warning: result of call to 'openSelected' is unused [#no-usage]
2990 |       openWithDefaultApp(item)
2991 |     case .note, .reveal:
2992 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2993 |     }
2994 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3024:9: warning: no 'async' operations occur within 'await' expression
3022 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3023 |       Task {
3024 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3025 |       }
3026 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3051:9: warning: no 'async' operations occur within 'await' expression
3049 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3050 |       Task {
3051 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3052 |       }
3053 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3109:9: warning: no 'async' operations occur within 'await' expression
3107 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3108 |       Task {
3109 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3110 |           itemID: item.id,
3111 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3140:9: warning: no 'async' operations occur within 'await' expression
3138 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3139 |       Task {
3140 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3141 |           itemID: item.id,
3142 |           title: item.title.text,
[170/193] Compiling BobMacCapture RefsPanelView.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:628:14: warning: no 'async' operations occur within 'await' expression
 626 |     }.store(in: &subscriptions)
 627 |     library.$scanState.sink { [weak self] _ in
 628 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:631:14: warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in
 631 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 632 |     }.store(in: &subscriptions)
 633 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2992:7: warning: result of call to 'openSelected' is unused [#no-usage]
2990 |       openWithDefaultApp(item)
2991 |     case .note, .reveal:
2992 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2993 |     }
2994 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3024:9: warning: no 'async' operations occur within 'await' expression
3022 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3023 |       Task {
3024 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3025 |       }
3026 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3051:9: warning: no 'async' operations occur within 'await' expression
3049 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3050 |       Task {
3051 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3052 |       }
3053 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3109:9: warning: no 'async' operations occur within 'await' expression
3107 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3108 |       Task {
3109 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3110 |           itemID: item.id,
3111 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3140:9: warning: no 'async' operations occur within 'await' expression
3138 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3139 |       Task {
3140 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3141 |           itemID: item.id,
3142 |           title: item.title.text,
[171/193] Compiling BobMacCapture RefsQuoteText.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:628:14: warning: no 'async' operations occur within 'await' expression
 626 |     }.store(in: &subscriptions)
 627 |     library.$scanState.sink { [weak self] _ in
 628 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:631:14: warning: no 'async' operations occur within 'await' expression
 629 |     }.store(in: &subscriptions)
 630 |     library.$refreshState.sink { [weak self] _ in
 631 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 632 |     }.store(in: &subscriptions)
 633 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2992:7: warning: result of call to 'openSelected' is unused [#no-usage]
2990 |       openWithDefaultApp(item)
2991 |     case .note, .reveal:
2992 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2993 |     }
2994 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3024:9: warning: no 'async' operations occur within 'await' expression
3022 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3023 |       Task {
3024 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3025 |       }
3026 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3051:9: warning: no 'async' operations occur within 'await' expression
3049 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3050 |       Task {
3051 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3052 |       }
3053 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3109:9: warning: no 'async' operations occur within 'await' expression
3107 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3108 |       Task {
3109 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3110 |           itemID: item.id,
3111 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3140:9: warning: no 'async' operations occur within 'await' expression
3138 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3139 |       Task {
3140 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3141 |           itemID: item.id,
3142 |           title: item.title.text,
[172/193] Compiling BobMacCapture AXHighlightsTabsReader.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
179 | @MainActor
180 | public final class RefsDecodedImageBudget {
181 |   public static let defaultByteLimit = RefsAnnotationImageLoader.bitmapCacheByteLimit
    |                     `- note: static property declared here
182 | 
183 |   private let byteLimit: Int
    :
186 |   public private(set) var byteCost = 0
187 | 
188 |   public init(byteLimit: Int = defaultByteLimit) {
    |                                `- warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
189 |     self.byteLimit = max(byteLimit, 1)
190 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[173/193] Compiling BobMacCapture RefsActionsMenu.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
179 | @MainActor
180 | public final class RefsDecodedImageBudget {
181 |   public static let defaultByteLimit = RefsAnnotationImageLoader.bitmapCacheByteLimit
    |                     `- note: static property declared here
182 | 
183 |   private let byteLimit: Int
    :
186 |   public private(set) var byteCost = 0
187 | 
188 |   public init(byteLimit: Int = defaultByteLimit) {
    |                                `- warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
189 |     self.byteLimit = max(byteLimit, 1)
190 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[174/193] Compiling BobMacCapture RefsAnnotationImages.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
179 | @MainActor
180 | public final class RefsDecodedImageBudget {
181 |   public static let defaultByteLimit = RefsAnnotationImageLoader.bitmapCacheByteLimit
    |                     `- note: static property declared here
182 | 
183 |   private let byteLimit: Int
    :
186 |   public private(set) var byteCost = 0
187 | 
188 |   public init(byteLimit: Int = defaultByteLimit) {
    |                                `- warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
189 |     self.byteLimit = max(byteLimit, 1)
190 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[175/193] Compiling BobMacCapture RefsCopyCardView.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
179 | @MainActor
180 | public final class RefsDecodedImageBudget {
181 |   public static let defaultByteLimit = RefsAnnotationImageLoader.bitmapCacheByteLimit
    |                     `- note: static property declared here
182 | 
183 |   private let byteLimit: Int
    :
186 |   public private(set) var byteCost = 0
187 | 
188 |   public init(byteLimit: Int = defaultByteLimit) {
    |                                `- warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
189 |     self.byteLimit = max(byteLimit, 1)
190 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[176/193] Compiling BobMacCapture RefsCopyHUD.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
179 | @MainActor
180 | public final class RefsDecodedImageBudget {
181 |   public static let defaultByteLimit = RefsAnnotationImageLoader.bitmapCacheByteLimit
    |                     `- note: static property declared here
182 | 
183 |   private let byteLimit: Int
    :
186 |   public private(set) var byteCost = 0
187 | 
188 |   public init(byteLimit: Int = defaultByteLimit) {
    |                                `- warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
189 |     self.byteLimit = max(byteLimit, 1)
190 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[177/193] Compiling BobMacCapture RefsFooter.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
179 | @MainActor
180 | public final class RefsDecodedImageBudget {
181 |   public static let defaultByteLimit = RefsAnnotationImageLoader.bitmapCacheByteLimit
    |                     `- note: static property declared here
182 | 
183 |   private let byteLimit: Int
    :
186 |   public private(set) var byteCost = 0
187 | 
188 |   public init(byteLimit: Int = defaultByteLimit) {
    |                                `- warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
189 |     self.byteLimit = max(byteLimit, 1)
190 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[178/193] Compiling BobMacCapture RefsInspectorImageViews.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
179 | @MainActor
180 | public final class RefsDecodedImageBudget {
181 |   public static let defaultByteLimit = RefsAnnotationImageLoader.bitmapCacheByteLimit
    |                     `- note: static property declared here
182 | 
183 |   private let byteLimit: Int
    :
186 |   public private(set) var byteCost = 0
187 | 
188 |   public init(byteLimit: Int = defaultByteLimit) {
    |                                `- warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
189 |     self.byteLimit = max(byteLimit, 1)
190 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[179/193] Compiling BobMacCapture RefsInspectorLoader.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
179 | @MainActor
180 | public final class RefsDecodedImageBudget {
181 |   public static let defaultByteLimit = RefsAnnotationImageLoader.bitmapCacheByteLimit
    |                     `- note: static property declared here
182 | 
183 |   private let byteLimit: Int
    :
186 |   public private(set) var byteCost = 0
187 | 
188 |   public init(byteLimit: Int = defaultByteLimit) {
    |                                `- warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
189 |     self.byteLimit = max(byteLimit, 1)
190 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[180/193] Compiling BobMacCapture RefsInspectorScroll.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
179 | @MainActor
180 | public final class RefsDecodedImageBudget {
181 |   public static let defaultByteLimit = RefsAnnotationImageLoader.bitmapCacheByteLimit
    |                     `- note: static property declared here
182 | 
183 |   private let byteLimit: Int
    :
186 |   public private(set) var byteCost = 0
187 | 
188 |   public init(byteLimit: Int = defaultByteLimit) {
    |                                `- warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
189 |     self.byteLimit = max(byteLimit, 1)
190 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[181/193] Emitting module BobMacCapture
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
865 |     }
866 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppDelegate.swift:864:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
862 |     openSettings: @escaping () -> Void = {},
863 |     activateApplication: @escaping () -> Void = {
864 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
865 |     }
866 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/AppSettings.swift:196:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
194 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
195 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
196 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
197 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
198 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
179 | @MainActor
180 | public final class RefsDecodedImageBudget {
181 |   public static let defaultByteLimit = RefsAnnotationImageLoader.bitmapCacheByteLimit
    |                     `- note: static property declared here
182 | 
183 |   private let byteLimit: Int
    :
186 |   public private(set) var byteCost = 0
187 | 
188 |   public init(byteLimit: Int = defaultByteLimit) {
    |                                `- warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
189 |     self.byteLimit = max(byteLimit, 1)
190 |   }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[182/193] Compiling BobMacCapture CapturePanelView.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[183/193] Compiling BobMacCapture CapturePanelWindowSizer.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[184/193] Compiling BobMacCapture CapturePickerFilterField.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[185/193] Compiling BobMacCapture CapturePickerState.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[186/193] Compiling BobMacCapture CapturePickerView.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[187/193] Compiling BobMacCapture CapturePlanBudgetMeterRow.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[188/193] Compiling BobMacCapture CapturePullInChoice.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[189/193] Compiling BobMacCapture CapturePullInChoiceView.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[190/193] Compiling BobMacCapture CaptureShowRefreshWindow.swift
/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.gpWDb2/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[190/193] Write Objects.LinkFileList
[191/193] Linking BobMacCapture
[192/193] Applying BobMacCapture
Build complete! (93.37s)
PASS BobMacCaptureTests
PASS BobMacCaptureInstallHelperTests
PASS CaptureCoreTests
PASS RefsCoreTests
Type-check only: macOS test targets were checked against a stub; CI still runs the tests.

