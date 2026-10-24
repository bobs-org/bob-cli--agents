# Chat History - ace-run (bob-cli-an.6.6.6.5.6.4--mon-2)

- **TIMESTAMP:** 2026-10-24 11:01:17 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-an.6.6.6.5.6.4--mon-2

## Prompt

sase monitor start --command 'ssh mac \'set -e; trap \'"\'"\'rm -rf -- /tmp/bob-mac-capture-argv-pQtZiugWXv\'"\'"\' EXIT; cd /tmp/bob-mac-capture-argv-pQtZiugWXv; ./Scripts/bundle.sh --identity -; just typecheck-tests\'' --reason 'Run bundle and test-target typecheck in disposable Mac scratch copy for mac-panel argv phase'

## Response

sase tool run c342bedd43fe0f8d3995686a5083f655
X11 forwarding request failed on channel 0
Building for production...
[0/6] Write sources
[3/6] Write swift-version--1AB21518FC5DEDBE.txt
[5/7] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[6/8] Compiling RefsCore RefsArrivals.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
903 |     }
904 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
903 |     }
904 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:81:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 79 |     NSApplication.shared.addSceneRepresentation(representation)
 80 |     settingsSceneRepresentation = representation
 81 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 82 |       representation.environment.openSettings()
 83 |     }
    :
897 |   var activateApplication: () -> Void
898 | 
899 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:285:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
283 |     menu.addItem(redo)
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
287 |     menu.addItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:286:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
287 |     menu.addItem(
288 |       NSMenuItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:295:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     )
294 |     menu.addItem(
295 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
296 |     return menu
297 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:492:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
490 |   /// off MainActor state.
491 |   nonisolated static func storedHighlightsAppPath() -> String {
492 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
493 |   }
494 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:572:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
570 |       library: library,
571 |       opener: WorkspaceRefsOpener(),
572 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
573 |       tabs: tabsSession,
574 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:808:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
806 |       return
807 |     }
808 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
809 |   }
810 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:204:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
202 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
203 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
204 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
205 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
206 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8833:23: warning: no 'async' operations occur within 'await' expression
 8831 |                 }
 8832 | 
 8833 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8834 |                     return
 8835 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8838:21: warning: no 'async' operations occur within 'await' expression
 8836 | 
 8837 |                 if pickerNeeded == nil {
 8838 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8839 |                         draft: draft,
 8840 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8852:27: warning: no 'async' operations occur within 'await' expression
 8850 |                     await completionGate.value
 8851 |                     try Task.checkCancellation()
 8852 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8853 |                         return
 8854 |                     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8859:20: warning: no 'async' operations occur within 'await' expression
 8857 |                 if let cursorUTF8Offset,
 8858 |                    requestCompletion,
 8859 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8860 |                        parse: parse,
 8861 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8865:37: warning: no 'async' operations occur within 'await' expression
 8863 |                    ) == true
 8864 |                 {
 8865 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8866 |                         parse: parse,
 8867 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:9094:28: warning: no 'async' operations occur within 'await' expression
 9092 |         Task { [weak self, processClient] in
 9093 |             do {
 9094 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 9095 |                 let processClientIdentity = processClient.identityToken
 9096 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:632:14: warning: no 'async' operations occur within 'await' expression
 630 |     }.store(in: &subscriptions)
 631 |     library.$scanState.sink { [weak self] _ in
 632 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:635:14: warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in
 635 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 636 |     }.store(in: &subscriptions)
 637 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3054:7: warning: result of call to 'openSelected' is unused [#no-usage]
3052 |       openWithDefaultApp(item)
3053 |     case .note, .reveal:
3054 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3055 |     }
3056 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3086:9: warning: no 'async' operations occur within 'await' expression
3084 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3085 |       Task {
3086 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3087 |       }
3088 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3113:9: warning: no 'async' operations occur within 'await' expression
3111 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3112 |       Task {
3113 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3114 |       }
3115 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3171:9: warning: no 'async' operations occur within 'await' expression
3169 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3170 |       Task {
3171 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3172 |           itemID: item.id,
3173 |           title: item.title.text,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3202:9: warning: no 'async' operations occur within 'await' expression
3200 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3201 |       Task {
3202 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3203 |           itemID: item.id,
3204 |           title: item.title.text,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
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
Build of product 'BobMacCapture' complete! (197.36s)
/tmp/bob-mac-capture-argv-pQtZiugWXv/.build/bundle/Bob Mac Capture.app/Contents/MacOS/BobMacCapture: replacing existing signature
/tmp/bob-mac-capture-argv-pQtZiugWXv/.build/bundle/Bob Mac Capture.app: replacing existing signature
/tmp/bob-mac-capture-argv-pQtZiugWXv/.build/bundle/Bob Mac Capture.app
./Scripts/typecheck-tests.sh
Building for debugging...
[0/18] Write sources
[5/18] Write BobMacCaptureInstallHelper-entitlement.plist
[5/18] Write BobMacCapture-entitlement.plist
[5/18] Write refs-rank-entitlement.plist
[8/18] Write swift-version--1AB21518FC5DEDBE.txt
[10/77] Emitting module CaptureCore
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[11/85] Compiling CaptureCore CapturePanelPlacement.swift
[12/85] Compiling CaptureCore CapturePickerHelpers.swift
[13/85] Compiling CaptureCore CapturePickerPresentation.swift
[14/85] Compiling CaptureCore CapturePlanBudgetPresentation.swift
[15/85] Compiling CaptureCore CapturePomodoroAdjustPresentation.swift
[16/85] Compiling CaptureCore CapturePomodoroBlockPresentation.swift
[17/85] Compiling CaptureCore CapturePomodoroClosePresentation.swift
[18/85] Compiling CaptureCore CapturePomodoroLineTokens.swift
[19/85] Compiling CaptureCore CaptureAgendaFitPlanner.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[20/85] Compiling CaptureCore CaptureAgendaHold.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[21/85] Compiling CaptureCore CaptureAgendaInlineText.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[22/85] Compiling CaptureCore CaptureAgendaLayout.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[23/85] Compiling CaptureCore CaptureAgendaModels.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[24/85] Compiling CaptureCore CaptureAgendaPresentation.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[25/85] Compiling CaptureCore CaptureAgendaRefreshFilter.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[26/85] Compiling CaptureCore CaptureAgendaRefreshState.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[27/85] Compiling CaptureCore CaptureAgendaVisibility.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[28/85] Compiling CaptureCore CapturePomodoroLinkPresentation.swift
[29/85] Compiling CaptureCore CapturePomodoroResetPresentation.swift
[30/85] Compiling CaptureCore CapturePomodoroShiftPresentation.swift
[31/85] Compiling CaptureCore CapturePomodoroStartPresentation.swift
[32/85] Compiling CaptureCore CaptureProjectNotePresentation.swift
[33/85] Compiling CaptureCore CaptureRefFileUnder.swift
[34/85] Compiling CaptureCore CaptureRefPresentation.swift
[35/85] Compiling CaptureCore CaptureRelatedModels.swift
[36/85] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[37/85] Compiling CaptureCore BlockIDPickerIndex.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[38/85] Compiling CaptureCore BlockIDRules.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[39/85] Compiling CaptureCore BobEnvironment.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[40/85] Compiling CaptureCore BobErrors.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[41/85] Compiling CaptureCore BobExecutableResolver.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[42/85] Compiling CaptureCore BobMacCaptureLaunchContext.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[43/85] Compiling CaptureCore BobProcessClient.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[44/85] Compiling CaptureCore CanceledDraftStashStore.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[45/85] Compiling CaptureCore CaptureRelationshipCopy.swift
[46/85] Compiling CaptureCore CaptureRelationshipPresentation.swift
[47/85] Compiling CaptureCore CaptureSavedTemplates.swift
[48/85] Compiling CaptureCore CaptureSubBulletPresentation.swift
[49/85] Compiling CaptureCore CaptureSuccessorPresentation.swift
[50/85] Compiling CaptureCore CaptureTargetsCache.swift
[51/85] Compiling CaptureCore CaptureTaskBlockPresentation.swift
[52/85] Compiling CaptureCore CaptureTaskCompletePresentation.swift
[53/85] Compiling CaptureCore CaptureTemplateStart.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[54/85] Compiling CaptureCore CaptureTextRanges.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[55/85] Compiling CaptureCore CaptureTodayPomodoroGoto.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[56/85] Compiling CaptureCore CaptureTogglePresentation.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[57/85] Compiling CaptureCore CompletionRowContent.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[58/85] Compiling CaptureCore DependencyPickerPresentation.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[59/85] Compiling CaptureCore FuzzyMatcher.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[60/85] Compiling CaptureCore ObsidianOpenURL.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[61/85] Compiling CaptureCore ParentTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[62/85] Compiling CaptureCore PomodoroHomes.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[63/85] Compiling CaptureCore SimilarTasksBandEdits.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[64/85] Compiling CaptureCore SimilarTasksBandPolicy.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[65/85] Compiling CaptureCore SimilarTasksBandPresentation.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[66/85] Compiling CaptureCore TaskCompletePickerPresentation.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[67/85] Compiling CaptureCore TaskDisplayText.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[68/85] Compiling CaptureCore TaskLinkPickerPresentation.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 | 
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
[69/85] Compiling CaptureCore CaptureBlockDiffRow.swift
[70/85] Compiling CaptureCore CaptureCloseTaskCommaAssist.swift
[71/85] Compiling CaptureCore CaptureCloseTaskCommaProvenance.swift
[72/85] Compiling CaptureCore CaptureEditWrite.swift
[73/85] Compiling CaptureCore CaptureLinkGuardPresentation.swift
[74/85] Compiling CaptureCore CaptureModels.swift
[75/85] Compiling CaptureCore CaptureOpenHintPresentation.swift
[76/85] Compiling CaptureCore CaptureOpenPlan.swift
[77/117] Emitting module RefsCore
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[78/120] Compiling RefsCore RefsInspectorImages.swift
[79/120] Compiling RefsCore RefsListScroll.swift
[80/120] Compiling RefsCore RefsModel.swift
[81/120] Compiling RefsCore RefsNew.swift
[82/120] Compiling RefsCore RefsSelection.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[83/120] Compiling RefsCore RefsStores.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[84/120] Compiling RefsCore RefsTabClose.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[85/120] Compiling RefsCore RefsTabsRanking.swift
[86/120] Compiling RefsCore RefsToday.swift
[87/120] Compiling RefsCore RefsTodayLinkCard.swift
[88/120] Compiling RefsCore RefsTodayLinkModels.swift
[89/120] Compiling RefsCore RefsTodayLinkPresentation.swift
[90/120] Compiling RefsCore RefsWatcherRelevance.swift
[91/120] Compiling RefsCore RefsFetching.swift
[92/120] Compiling RefsCore RefsHighlightPicker.swift
[93/120] Compiling RefsCore RefsHighlightsTabs.swift
[94/120] Compiling RefsCore RefsInspector.swift
[95/120] Compiling RefsCore RefsArrivals.swift
[96/120] Compiling RefsCore RefsCaption.swift
[97/120] Compiling RefsCore RefsCopy.swift
[98/120] Compiling RefsCore RefsDecoding.swift
[99/120] Compiling RefsCore RefsRanking.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {
[100/120] Compiling RefsCore RefsRename.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {
[101/120] Compiling RefsCore RefsScan.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {
[102/120] Compiling RefsCore RefsScanReceipt.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {
[103/120] Compiling RefsCore RefsNewest.swift
[104/120] Compiling RefsCore RefsPDFUpdates.swift
[105/120] Compiling RefsCore RefsPanelGeometry.swift
[106/120] Compiling RefsCore RefsQuoteUnderline.swift
[107/187] Compiling refs_rank main.swift
[108/187] Emitting module refs_rank
[108/187] Write Objects.LinkFileList
[109/187] Linking refs-rank
[110/187] Applying refs-rank
[112/187] Compiling BobMacCaptureInstallHelper InstallRelauncher.swift
[113/187] Emitting module BobMacCaptureInstallHelper
[114/187] Compiling BobMacCaptureInstallHelper InstallHelperArguments.swift
[115/187] Compiling BobMacCaptureInstallHelper InstallHelperError.swift
[116/187] Compiling BobMacCaptureInstallHelper BobMacCaptureInstallHelperMain.swift
[116/187] Write Objects.LinkFileList
[117/187] Linking BobMacCaptureInstallHelper
[118/187] Applying BobMacCaptureInstallHelper
[120/187] Emitting module BobMacCapture
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
903 |     }
904 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
903 |     }
904 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:204:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
202 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
203 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
204 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
205 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
206 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[121/196] Compiling BobMacCapture AccessibilityTrust.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
903 |     }
904 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
903 |     }
904 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:81:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 79 |     NSApplication.shared.addSceneRepresentation(representation)
 80 |     settingsSceneRepresentation = representation
 81 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 82 |       representation.environment.openSettings()
 83 |     }
    :
897 |   var activateApplication: () -> Void
898 | 
899 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:285:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
283 |     menu.addItem(redo)
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
287 |     menu.addItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:286:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
287 |     menu.addItem(
288 |       NSMenuItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:295:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     )
294 |     menu.addItem(
295 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
296 |     return menu
297 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:492:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
490 |   /// off MainActor state.
491 |   nonisolated static func storedHighlightsAppPath() -> String {
492 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
493 |   }
494 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:572:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
570 |       library: library,
571 |       opener: WorkspaceRefsOpener(),
572 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
573 |       tabs: tabsSession,
574 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:808:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
806 |       return
807 |     }
808 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
809 |   }
810 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:204:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
202 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
203 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
204 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
205 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
206 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[122/196] Compiling BobMacCapture AppDelegate.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
903 |     }
904 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
903 |     }
904 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:81:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 79 |     NSApplication.shared.addSceneRepresentation(representation)
 80 |     settingsSceneRepresentation = representation
 81 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 82 |       representation.environment.openSettings()
 83 |     }
    :
897 |   var activateApplication: () -> Void
898 | 
899 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:285:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
283 |     menu.addItem(redo)
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
287 |     menu.addItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:286:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
287 |     menu.addItem(
288 |       NSMenuItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:295:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     )
294 |     menu.addItem(
295 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
296 |     return menu
297 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:492:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
490 |   /// off MainActor state.
491 |   nonisolated static func storedHighlightsAppPath() -> String {
492 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
493 |   }
494 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:572:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
570 |       library: library,
571 |       opener: WorkspaceRefsOpener(),
572 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
573 |       tabs: tabsSession,
574 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:808:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
806 |       return
807 |     }
808 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
809 |   }
810 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:204:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
202 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
203 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
204 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
205 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
206 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[123/196] Compiling BobMacCapture AppRelauncher.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
903 |     }
904 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
903 |     }
904 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:81:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 79 |     NSApplication.shared.addSceneRepresentation(representation)
 80 |     settingsSceneRepresentation = representation
 81 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 82 |       representation.environment.openSettings()
 83 |     }
    :
897 |   var activateApplication: () -> Void
898 | 
899 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:285:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
283 |     menu.addItem(redo)
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
287 |     menu.addItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:286:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
287 |     menu.addItem(
288 |       NSMenuItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:295:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     )
294 |     menu.addItem(
295 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
296 |     return menu
297 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:492:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
490 |   /// off MainActor state.
491 |   nonisolated static func storedHighlightsAppPath() -> String {
492 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
493 |   }
494 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:572:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
570 |       library: library,
571 |       opener: WorkspaceRefsOpener(),
572 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
573 |       tabs: tabsSession,
574 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:808:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
806 |       return
807 |     }
808 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
809 |   }
810 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:204:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
202 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
203 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
204 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
205 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
206 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[124/196] Compiling BobMacCapture AppSettings.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
903 |     }
904 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
903 |     }
904 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:81:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 79 |     NSApplication.shared.addSceneRepresentation(representation)
 80 |     settingsSceneRepresentation = representation
 81 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 82 |       representation.environment.openSettings()
 83 |     }
    :
897 |   var activateApplication: () -> Void
898 | 
899 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:285:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
283 |     menu.addItem(redo)
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
287 |     menu.addItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:286:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
287 |     menu.addItem(
288 |       NSMenuItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:295:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     )
294 |     menu.addItem(
295 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
296 |     return menu
297 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:492:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
490 |   /// off MainActor state.
491 |   nonisolated static func storedHighlightsAppPath() -> String {
492 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
493 |   }
494 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:572:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
570 |       library: library,
571 |       opener: WorkspaceRefsOpener(),
572 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
573 |       tabs: tabsSession,
574 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:808:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
806 |       return
807 |     }
808 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
809 |   }
810 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:204:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
202 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
203 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
204 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
205 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
206 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[125/196] Compiling BobMacCapture BlockDiffCard.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
903 |     }
904 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
903 |     }
904 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:81:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 79 |     NSApplication.shared.addSceneRepresentation(representation)
 80 |     settingsSceneRepresentation = representation
 81 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 82 |       representation.environment.openSettings()
 83 |     }
    :
897 |   var activateApplication: () -> Void
898 | 
899 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:285:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
283 |     menu.addItem(redo)
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
287 |     menu.addItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:286:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
287 |     menu.addItem(
288 |       NSMenuItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:295:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     )
294 |     menu.addItem(
295 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
296 |     return menu
297 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:492:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
490 |   /// off MainActor state.
491 |   nonisolated static func storedHighlightsAppPath() -> String {
492 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
493 |   }
494 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:572:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
570 |       library: library,
571 |       opener: WorkspaceRefsOpener(),
572 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
573 |       tabs: tabsSession,
574 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:808:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
806 |       return
807 |     }
808 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
809 |   }
810 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:204:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
202 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
203 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
204 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
205 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
206 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[126/196] Compiling BobMacCapture BlockIDField.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
903 |     }
904 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
903 |     }
904 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:81:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 79 |     NSApplication.shared.addSceneRepresentation(representation)
 80 |     settingsSceneRepresentation = representation
 81 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 82 |       representation.environment.openSettings()
 83 |     }
    :
897 |   var activateApplication: () -> Void
898 | 
899 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:285:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
283 |     menu.addItem(redo)
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
287 |     menu.addItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:286:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
287 |     menu.addItem(
288 |       NSMenuItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:295:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     )
294 |     menu.addItem(
295 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
296 |     return menu
297 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:492:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
490 |   /// off MainActor state.
491 |   nonisolated static func storedHighlightsAppPath() -> String {
492 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
493 |   }
494 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:572:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
570 |       library: library,
571 |       opener: WorkspaceRefsOpener(),
572 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
573 |       tabs: tabsSession,
574 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:808:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
806 |       return
807 |     }
808 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
809 |   }
810 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:204:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
202 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
203 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
204 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
205 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
206 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[127/196] Compiling BobMacCapture BobMacCaptureMain.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
903 |     }
904 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
903 |     }
904 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:81:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 79 |     NSApplication.shared.addSceneRepresentation(representation)
 80 |     settingsSceneRepresentation = representation
 81 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 82 |       representation.environment.openSettings()
 83 |     }
    :
897 |   var activateApplication: () -> Void
898 | 
899 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:285:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
283 |     menu.addItem(redo)
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
287 |     menu.addItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:286:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
287 |     menu.addItem(
288 |       NSMenuItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:295:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     )
294 |     menu.addItem(
295 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
296 |     return menu
297 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:492:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
490 |   /// off MainActor state.
491 |   nonisolated static func storedHighlightsAppPath() -> String {
492 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
493 |   }
494 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:572:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
570 |       library: library,
571 |       opener: WorkspaceRefsOpener(),
572 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
573 |       tabs: tabsSession,
574 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:808:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
806 |       return
807 |     }
808 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
809 |   }
810 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:204:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
202 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
203 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
204 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
205 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
206 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[128/196] Compiling BobMacCapture BobPanelCoordinator.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
903 |     }
904 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
903 |     }
904 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:81:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 79 |     NSApplication.shared.addSceneRepresentation(representation)
 80 |     settingsSceneRepresentation = representation
 81 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 82 |       representation.environment.openSettings()
 83 |     }
    :
897 |   var activateApplication: () -> Void
898 | 
899 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:285:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
283 |     menu.addItem(redo)
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
287 |     menu.addItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:286:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
287 |     menu.addItem(
288 |       NSMenuItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:295:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     )
294 |     menu.addItem(
295 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
296 |     return menu
297 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:492:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
490 |   /// off MainActor state.
491 |   nonisolated static func storedHighlightsAppPath() -> String {
492 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
493 |   }
494 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:572:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
570 |       library: library,
571 |       opener: WorkspaceRefsOpener(),
572 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
573 |       tabs: tabsSession,
574 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:808:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
806 |       return
807 |     }
808 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
809 |   }
810 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:204:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
202 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
203 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
204 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
205 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
206 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[129/196] Compiling BobMacCapture BundleSigningInspector.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
903 |     }
904 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
903 |     }
904 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:81:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 79 |     NSApplication.shared.addSceneRepresentation(representation)
 80 |     settingsSceneRepresentation = representation
 81 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 82 |       representation.environment.openSettings()
 83 |     }
    :
897 |   var activateApplication: () -> Void
898 | 
899 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:285:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
283 |     menu.addItem(redo)
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
287 |     menu.addItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:286:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
287 |     menu.addItem(
288 |       NSMenuItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:295:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     )
294 |     menu.addItem(
295 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
296 |     return menu
297 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:492:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
490 |   /// off MainActor state.
491 |   nonisolated static func storedHighlightsAppPath() -> String {
492 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
493 |   }
494 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:572:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
570 |       library: library,
571 |       opener: WorkspaceRefsOpener(),
572 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
573 |       tabs: tabsSession,
574 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:808:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
806 |       return
807 |     }
808 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
809 |   }
810 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:204:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
202 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
203 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
204 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
205 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
206 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[130/196] Compiling BobMacCapture CanceledDraftStash.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
903 |     }
904 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:902:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {
902 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
903 |     }
904 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:81:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 79 |     NSApplication.shared.addSceneRepresentation(representation)
 80 |     settingsSceneRepresentation = representation
 81 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 82 |       representation.environment.openSettings()
 83 |     }
    :
897 |   var activateApplication: () -> Void
898 | 
899 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
900 |     openSettings: @escaping () -> Void = {},
901 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:285:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
283 |     menu.addItem(redo)
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
287 |     menu.addItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:286:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
287 |     menu.addItem(
288 |       NSMenuItem(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:295:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     )
294 |     menu.addItem(
295 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
296 |     return menu
297 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:492:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
490 |   /// off MainActor state.
491 |   nonisolated static func storedHighlightsAppPath() -> String {
492 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
493 |   }
494 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:572:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
570 |       library: library,
571 |       opener: WorkspaceRefsOpener(),
572 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
573 |       tabs: tabsSession,
574 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppDelegate.swift:808:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
806 |       return
807 |     }
808 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
809 |   }
810 | 

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/AppSettings.swift:204:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
202 |     static let refsHighlightsOpenKey = "refsHighlightsOpenKey"
203 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
204 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
205 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
206 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[131/196] Compiling BobMacCapture CaptureTargetsRefreshGate.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.
[132/196] Compiling BobMacCapture HighlightsTakeover.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.
[133/196] Compiling BobMacCapture HotKeyRegistry.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.
[134/196] Compiling BobMacCapture NotificationService.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.
[135/196] Compiling BobMacCapture PlainTextPaste.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.
[136/196] Compiling BobMacCapture PomodoroBlockView.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.
[137/196] Compiling BobMacCapture PomodoroHomeColor.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.
[138/196] Compiling BobMacCapture PomodoroNameField.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.
[139/196] Compiling BobMacCapture AXHighlightsTabsReader.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.
[140/196] Compiling BobMacCapture RefsRowView.swift
[141/196] Compiling BobMacCapture RefsScanReceiptObserver.swift
[142/196] Compiling BobMacCapture RefsSearchBar.swift
[143/196] Compiling BobMacCapture RefsTabsViews.swift
[144/196] Compiling BobMacCapture RefsTodayLinkCardView.swift
[145/196] Compiling BobMacCapture RefsUnderlineRenderer.swift
[146/196] Compiling BobMacCapture RefsVisualTokens.swift
[147/196] Compiling BobMacCapture RefsHighlightsOpenKey.swift
[148/196] Compiling BobMacCapture RefsHighlightsTabsKey.swift
[149/196] Compiling BobMacCapture RefsHotkeyRegistration.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[150/196] Compiling BobMacCapture SavedTemplateShelf.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[151/196] Compiling BobMacCapture SettingsView.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[152/196] Compiling BobMacCapture Signposts.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[153/196] Compiling BobMacCapture SimilarTasksBandView.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[154/196] Compiling BobMacCapture StatusItemController.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[155/196] Compiling BobMacCapture StatusItemGlyph.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[156/196] Compiling BobMacCapture TaskBlockView.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[157/196] Compiling BobMacCapture VaultTargetWatcher.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[158/196] Compiling BobMacCapture CapturePanelWindowSizer.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[159/196] Compiling BobMacCapture CapturePickerFilterField.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[160/196] Compiling BobMacCapture CapturePickerState.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[161/196] Compiling BobMacCapture CapturePickerView.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[162/196] Compiling BobMacCapture CapturePlanBudgetMeterRow.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[163/196] Compiling BobMacCapture CapturePullInChoice.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[164/196] Compiling BobMacCapture CapturePullInChoiceView.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[165/196] Compiling BobMacCapture CaptureShowRefreshWindow.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[166/196] Compiling BobMacCapture CaptureSnippetResolver.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 | 
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 | 
 159 |   private var fetcher: RefsFetching?

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[167/196] Compiling BobMacCapture RefsKeyRouter.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:632:14: warning: no 'async' operations occur within 'await' expression
 630 |     }.store(in: &subscriptions)
 631 |     library.$scanState.sink { [weak self] _ in
 632 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:635:14: warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in
 635 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 636 |     }.store(in: &subscriptions)
 637 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3054:7: warning: result of call to 'openSelected' is unused [#no-usage]
3052 |       openWithDefaultApp(item)
3053 |     case .note, .reveal:
3054 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3055 |     }
3056 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3086:9: warning: no 'async' operations occur within 'await' expression
3084 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3085 |       Task {
3086 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3087 |       }
3088 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3113:9: warning: no 'async' operations occur within 'await' expression
3111 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3112 |       Task {
3113 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3114 |       }
3115 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3171:9: warning: no 'async' operations occur within 'await' expression
3169 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3170 |       Task {
3171 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3172 |           itemID: item.id,
3173 |           title: item.title.text,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3202:9: warning: no 'async' operations occur within 'await' expression
3200 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3201 |       Task {
3202 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3203 |           itemID: item.id,
3204 |           title: item.title.text,
[168/196] Compiling BobMacCapture RefsLibrary.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:632:14: warning: no 'async' operations occur within 'await' expression
 630 |     }.store(in: &subscriptions)
 631 |     library.$scanState.sink { [weak self] _ in
 632 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:635:14: warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in
 635 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 636 |     }.store(in: &subscriptions)
 637 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3054:7: warning: result of call to 'openSelected' is unused [#no-usage]
3052 |       openWithDefaultApp(item)
3053 |     case .note, .reveal:
3054 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3055 |     }
3056 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3086:9: warning: no 'async' operations occur within 'await' expression
3084 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3085 |       Task {
3086 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3087 |       }
3088 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3113:9: warning: no 'async' operations occur within 'await' expression
3111 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3112 |       Task {
3113 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3114 |       }
3115 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3171:9: warning: no 'async' operations occur within 'await' expression
3169 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3170 |       Task {
3171 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3172 |           itemID: item.id,
3173 |           title: item.title.text,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3202:9: warning: no 'async' operations occur within 'await' expression
3200 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3201 |       Task {
3202 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3203 |           itemID: item.id,
3204 |           title: item.title.text,
[169/196] Compiling BobMacCapture RefsListView.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:632:14: warning: no 'async' operations occur within 'await' expression
 630 |     }.store(in: &subscriptions)
 631 |     library.$scanState.sink { [weak self] _ in
 632 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:635:14: warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in
 635 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 636 |     }.store(in: &subscriptions)
 637 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3054:7: warning: result of call to 'openSelected' is unused [#no-usage]
3052 |       openWithDefaultApp(item)
3053 |     case .note, .reveal:
3054 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3055 |     }
3056 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3086:9: warning: no 'async' operations occur within 'await' expression
3084 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3085 |       Task {
3086 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3087 |       }
3088 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3113:9: warning: no 'async' operations occur within 'await' expression
3111 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3112 |       Task {
3113 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3114 |       }
3115 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3171:9: warning: no 'async' operations occur within 'await' expression
3169 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3170 |       Task {
3171 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3172 |           itemID: item.id,
3173 |           title: item.title.text,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3202:9: warning: no 'async' operations occur within 'await' expression
3200 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3201 |       Task {
3202 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3203 |           itemID: item.id,
3204 |           title: item.title.text,
[170/196] Compiling BobMacCapture RefsPanel.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:632:14: warning: no 'async' operations occur within 'await' expression
 630 |     }.store(in: &subscriptions)
 631 |     library.$scanState.sink { [weak self] _ in
 632 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:635:14: warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in
 635 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 636 |     }.store(in: &subscriptions)
 637 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3054:7: warning: result of call to 'openSelected' is unused [#no-usage]
3052 |       openWithDefaultApp(item)
3053 |     case .note, .reveal:
3054 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3055 |     }
3056 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3086:9: warning: no 'async' operations occur within 'await' expression
3084 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3085 |       Task {
3086 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3087 |       }
3088 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3113:9: warning: no 'async' operations occur within 'await' expression
3111 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3112 |       Task {
3113 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3114 |       }
3115 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3171:9: warning: no 'async' operations occur within 'await' expression
3169 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3170 |       Task {
3171 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3172 |           itemID: item.id,
3173 |           title: item.title.text,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3202:9: warning: no 'async' operations occur within 'await' expression
3200 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3201 |       Task {
3202 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3203 |           itemID: item.id,
3204 |           title: item.title.text,
[171/196] Compiling BobMacCapture RefsPanelModel.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:632:14: warning: no 'async' operations occur within 'await' expression
 630 |     }.store(in: &subscriptions)
 631 |     library.$scanState.sink { [weak self] _ in
 632 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:635:14: warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in
 635 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 636 |     }.store(in: &subscriptions)
 637 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3054:7: warning: result of call to 'openSelected' is unused [#no-usage]
3052 |       openWithDefaultApp(item)
3053 |     case .note, .reveal:
3054 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3055 |     }
3056 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3086:9: warning: no 'async' operations occur within 'await' expression
3084 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3085 |       Task {
3086 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3087 |       }
3088 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3113:9: warning: no 'async' operations occur within 'await' expression
3111 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3112 |       Task {
3113 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3114 |       }
3115 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3171:9: warning: no 'async' operations occur within 'await' expression
3169 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3170 |       Task {
3171 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3172 |           itemID: item.id,
3173 |           title: item.title.text,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3202:9: warning: no 'async' operations occur within 'await' expression
3200 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3201 |       Task {
3202 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3203 |           itemID: item.id,
3204 |           title: item.title.text,
[172/196] Compiling BobMacCapture RefsPanelStates.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:632:14: warning: no 'async' operations occur within 'await' expression
 630 |     }.store(in: &subscriptions)
 631 |     library.$scanState.sink { [weak self] _ in
 632 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:635:14: warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in
 635 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 636 |     }.store(in: &subscriptions)
 637 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3054:7: warning: result of call to 'openSelected' is unused [#no-usage]
3052 |       openWithDefaultApp(item)
3053 |     case .note, .reveal:
3054 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3055 |     }
3056 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3086:9: warning: no 'async' operations occur within 'await' expression
3084 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3085 |       Task {
3086 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3087 |       }
3088 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3113:9: warning: no 'async' operations occur within 'await' expression
3111 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3112 |       Task {
3113 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3114 |       }
3115 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3171:9: warning: no 'async' operations occur within 'await' expression
3169 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3170 |       Task {
3171 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3172 |           itemID: item.id,
3173 |           title: item.title.text,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3202:9: warning: no 'async' operations occur within 'await' expression
3200 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3201 |       Task {
3202 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3203 |           itemID: item.id,
3204 |           title: item.title.text,
[173/196] Compiling BobMacCapture RefsPanelView.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:632:14: warning: no 'async' operations occur within 'await' expression
 630 |     }.store(in: &subscriptions)
 631 |     library.$scanState.sink { [weak self] _ in
 632 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:635:14: warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in
 635 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 636 |     }.store(in: &subscriptions)
 637 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3054:7: warning: result of call to 'openSelected' is unused [#no-usage]
3052 |       openWithDefaultApp(item)
3053 |     case .note, .reveal:
3054 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3055 |     }
3056 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3086:9: warning: no 'async' operations occur within 'await' expression
3084 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3085 |       Task {
3086 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3087 |       }
3088 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3113:9: warning: no 'async' operations occur within 'await' expression
3111 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3112 |       Task {
3113 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3114 |       }
3115 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3171:9: warning: no 'async' operations occur within 'await' expression
3169 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3170 |       Task {
3171 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3172 |           itemID: item.id,
3173 |           title: item.title.text,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3202:9: warning: no 'async' operations occur within 'await' expression
3200 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3201 |       Task {
3202 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3203 |           itemID: item.id,
3204 |           title: item.title.text,
[174/196] Compiling BobMacCapture RefsQuoteText.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:632:14: warning: no 'async' operations occur within 'await' expression
 630 |     }.store(in: &subscriptions)
 631 |     library.$scanState.sink { [weak self] _ in
 632 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:635:14: warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in
 635 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 636 |     }.store(in: &subscriptions)
 637 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3054:7: warning: result of call to 'openSelected' is unused [#no-usage]
3052 |       openWithDefaultApp(item)
3053 |     case .note, .reveal:
3054 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3055 |     }
3056 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3086:9: warning: no 'async' operations occur within 'await' expression
3084 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3085 |       Task {
3086 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3087 |       }
3088 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3113:9: warning: no 'async' operations occur within 'await' expression
3111 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3112 |       Task {
3113 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3114 |       }
3115 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3171:9: warning: no 'async' operations occur within 'await' expression
3169 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3170 |       Task {
3171 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3172 |           itemID: item.id,
3173 |           title: item.title.text,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3202:9: warning: no 'async' operations occur within 'await' expression
3200 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3201 |       Task {
3202 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3203 |           itemID: item.id,
3204 |           title: item.title.text,
[175/196] Compiling BobMacCapture RefsRenameCardView.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 | 
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:632:14: warning: no 'async' operations occur within 'await' expression
 630 |     }.store(in: &subscriptions)
 631 |     library.$scanState.sink { [weak self] _ in
 632 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:635:14: warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in
 635 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 636 |     }.store(in: &subscriptions)
 637 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3054:7: warning: result of call to 'openSelected' is unused [#no-usage]
3052 |       openWithDefaultApp(item)
3053 |     case .note, .reveal:
3054 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3055 |     }
3056 |   }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3086:9: warning: no 'async' operations occur within 'await' expression
3084 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3085 |       Task {
3086 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3087 |       }
3088 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3113:9: warning: no 'async' operations occur within 'await' expression
3111 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3112 |       Task {
3113 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3114 |       }
3115 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3171:9: warning: no 'async' operations occur within 'await' expression
3169 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3170 |       Task {
3171 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3172 |           itemID: item.id,
3173 |           title: item.title.text,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3202:9: warning: no 'async' operations occur within 'await' expression
3200 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3201 |       Task {
3202 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3203 |           itemID: item.id,
3204 |           title: item.title.text,
[176/196] Compiling BobMacCapture CaptureAgendaRowMeasurer.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8833:23: warning: no 'async' operations occur within 'await' expression
 8831 |                 }
 8832 | 
 8833 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8834 |                     return
 8835 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8838:21: warning: no 'async' operations occur within 'await' expression
 8836 | 
 8837 |                 if pickerNeeded == nil {
 8838 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8839 |                         draft: draft,
 8840 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8852:27: warning: no 'async' operations occur within 'await' expression
 8850 |                     await completionGate.value
 8851 |                     try Task.checkCancellation()
 8852 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8853 |                         return
 8854 |                     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8859:20: warning: no 'async' operations occur within 'await' expression
 8857 |                 if let cursorUTF8Offset,
 8858 |                    requestCompletion,
 8859 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8860 |                        parse: parse,
 8861 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8865:37: warning: no 'async' operations occur within 'await' expression
 8863 |                    ) == true
 8864 |                 {
 8865 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8866 |                         parse: parse,
 8867 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:9094:28: warning: no 'async' operations occur within 'await' expression
 9092 |         Task { [weak self, processClient] in
 9093 |             do {
 9094 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 9095 |                 let processClientIdentity = processClient.identityToken
 9096 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[177/196] Compiling BobMacCapture CaptureAgendaStore.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8833:23: warning: no 'async' operations occur within 'await' expression
 8831 |                 }
 8832 | 
 8833 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8834 |                     return
 8835 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8838:21: warning: no 'async' operations occur within 'await' expression
 8836 | 
 8837 |                 if pickerNeeded == nil {
 8838 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8839 |                         draft: draft,
 8840 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8852:27: warning: no 'async' operations occur within 'await' expression
 8850 |                     await completionGate.value
 8851 |                     try Task.checkCancellation()
 8852 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8853 |                         return
 8854 |                     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8859:20: warning: no 'async' operations occur within 'await' expression
 8857 |                 if let cursorUTF8Offset,
 8858 |                    requestCompletion,
 8859 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8860 |                        parse: parse,
 8861 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8865:37: warning: no 'async' operations occur within 'await' expression
 8863 |                    ) == true
 8864 |                 {
 8865 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8866 |                         parse: parse,
 8867 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:9094:28: warning: no 'async' operations occur within 'await' expression
 9092 |         Task { [weak self, processClient] in
 9093 |             do {
 9094 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 9095 |                 let processClientIdentity = processClient.identityToken
 9096 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[178/196] Compiling BobMacCapture CaptureAgendaView.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8833:23: warning: no 'async' operations occur within 'await' expression
 8831 |                 }
 8832 | 
 8833 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8834 |                     return
 8835 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8838:21: warning: no 'async' operations occur within 'await' expression
 8836 | 
 8837 |                 if pickerNeeded == nil {
 8838 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8839 |                         draft: draft,
 8840 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8852:27: warning: no 'async' operations occur within 'await' expression
 8850 |                     await completionGate.value
 8851 |                     try Task.checkCancellation()
 8852 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8853 |                         return
 8854 |                     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8859:20: warning: no 'async' operations occur within 'await' expression
 8857 |                 if let cursorUTF8Offset,
 8858 |                    requestCompletion,
 8859 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8860 |                        parse: parse,
 8861 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8865:37: warning: no 'async' operations occur within 'await' expression
 8863 |                    ) == true
 8864 |                 {
 8865 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8866 |                         parse: parse,
 8867 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:9094:28: warning: no 'async' operations occur within 'await' expression
 9092 |         Task { [weak self, processClient] in
 9093 |             do {
 9094 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 9095 |                 let processClientIdentity = processClient.identityToken
 9096 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[179/196] Compiling BobMacCapture CaptureEditorPalette.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8833:23: warning: no 'async' operations occur within 'await' expression
 8831 |                 }
 8832 | 
 8833 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8834 |                     return
 8835 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8838:21: warning: no 'async' operations occur within 'await' expression
 8836 | 
 8837 |                 if pickerNeeded == nil {
 8838 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8839 |                         draft: draft,
 8840 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8852:27: warning: no 'async' operations occur within 'await' expression
 8850 |                     await completionGate.value
 8851 |                     try Task.checkCancellation()
 8852 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8853 |                         return
 8854 |                     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8859:20: warning: no 'async' operations occur within 'await' expression
 8857 |                 if let cursorUTF8Offset,
 8858 |                    requestCompletion,
 8859 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8860 |                        parse: parse,
 8861 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8865:37: warning: no 'async' operations occur within 'await' expression
 8863 |                    ) == true
 8864 |                 {
 8865 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8866 |                         parse: parse,
 8867 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:9094:28: warning: no 'async' operations occur within 'await' expression
 9092 |         Task { [weak self, processClient] in
 9093 |             do {
 9094 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 9095 |                 let processClientIdentity = processClient.identityToken
 9096 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[180/196] Compiling BobMacCapture CaptureEditorTextConfiguration.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8833:23: warning: no 'async' operations occur within 'await' expression
 8831 |                 }
 8832 | 
 8833 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8834 |                     return
 8835 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8838:21: warning: no 'async' operations occur within 'await' expression
 8836 | 
 8837 |                 if pickerNeeded == nil {
 8838 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8839 |                         draft: draft,
 8840 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8852:27: warning: no 'async' operations occur within 'await' expression
 8850 |                     await completionGate.value
 8851 |                     try Task.checkCancellation()
 8852 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8853 |                         return
 8854 |                     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8859:20: warning: no 'async' operations occur within 'await' expression
 8857 |                 if let cursorUTF8Offset,
 8858 |                    requestCompletion,
 8859 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8860 |                        parse: parse,
 8861 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8865:37: warning: no 'async' operations occur within 'await' expression
 8863 |                    ) == true
 8864 |                 {
 8865 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8866 |                         parse: parse,
 8867 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:9094:28: warning: no 'async' operations occur within 'await' expression
 9092 |         Task { [weak self, processClient] in
 9093 |             do {
 9094 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 9095 |                 let processClientIdentity = processClient.identityToken
 9096 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[181/196] Compiling BobMacCapture CaptureKeyCommandRouter.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8833:23: warning: no 'async' operations occur within 'await' expression
 8831 |                 }
 8832 | 
 8833 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8834 |                     return
 8835 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8838:21: warning: no 'async' operations occur within 'await' expression
 8836 | 
 8837 |                 if pickerNeeded == nil {
 8838 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8839 |                         draft: draft,
 8840 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8852:27: warning: no 'async' operations occur within 'await' expression
 8850 |                     await completionGate.value
 8851 |                     try Task.checkCancellation()
 8852 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8853 |                         return
 8854 |                     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8859:20: warning: no 'async' operations occur within 'await' expression
 8857 |                 if let cursorUTF8Offset,
 8858 |                    requestCompletion,
 8859 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8860 |                        parse: parse,
 8861 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8865:37: warning: no 'async' operations occur within 'await' expression
 8863 |                    ) == true
 8864 |                 {
 8865 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8866 |                         parse: parse,
 8867 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:9094:28: warning: no 'async' operations occur within 'await' expression
 9092 |         Task { [weak self, processClient] in
 9093 |             do {
 9094 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 9095 |                 let processClientIdentity = processClient.identityToken
 9096 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[182/196] Compiling BobMacCapture CapturePanelController.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8833:23: warning: no 'async' operations occur within 'await' expression
 8831 |                 }
 8832 | 
 8833 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8834 |                     return
 8835 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8838:21: warning: no 'async' operations occur within 'await' expression
 8836 | 
 8837 |                 if pickerNeeded == nil {
 8838 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8839 |                         draft: draft,
 8840 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8852:27: warning: no 'async' operations occur within 'await' expression
 8850 |                     await completionGate.value
 8851 |                     try Task.checkCancellation()
 8852 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8853 |                         return
 8854 |                     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8859:20: warning: no 'async' operations occur within 'await' expression
 8857 |                 if let cursorUTF8Offset,
 8858 |                    requestCompletion,
 8859 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8860 |                        parse: parse,
 8861 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8865:37: warning: no 'async' operations occur within 'await' expression
 8863 |                    ) == true
 8864 |                 {
 8865 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8866 |                         parse: parse,
 8867 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:9094:28: warning: no 'async' operations occur within 'await' expression
 9092 |         Task { [weak self, processClient] in
 9093 |             do {
 9094 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 9095 |                 let processClientIdentity = processClient.identityToken
 9096 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[183/196] Compiling BobMacCapture CapturePanelModel.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8833:23: warning: no 'async' operations occur within 'await' expression
 8831 |                 }
 8832 | 
 8833 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8834 |                     return
 8835 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8838:21: warning: no 'async' operations occur within 'await' expression
 8836 | 
 8837 |                 if pickerNeeded == nil {
 8838 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8839 |                         draft: draft,
 8840 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8852:27: warning: no 'async' operations occur within 'await' expression
 8850 |                     await completionGate.value
 8851 |                     try Task.checkCancellation()
 8852 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8853 |                         return
 8854 |                     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8859:20: warning: no 'async' operations occur within 'await' expression
 8857 |                 if let cursorUTF8Offset,
 8858 |                    requestCompletion,
 8859 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8860 |                        parse: parse,
 8861 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8865:37: warning: no 'async' operations occur within 'await' expression
 8863 |                    ) == true
 8864 |                 {
 8865 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8866 |                         parse: parse,
 8867 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:9094:28: warning: no 'async' operations occur within 'await' expression
 9092 |         Task { [weak self, processClient] in
 9093 |             do {
 9094 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 9095 |                 let processClientIdentity = processClient.identityToken
 9096 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[184/196] Compiling BobMacCapture CapturePanelView.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:2042:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2040 |                         refuseOverride: !allowsOverride,
 2041 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2042 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2043 |                     )
 2044 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8833:23: warning: no 'async' operations occur within 'await' expression
 8831 |                 }
 8832 | 
 8833 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8834 |                     return
 8835 |                 }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8838:21: warning: no 'async' operations occur within 'await' expression
 8836 | 
 8837 |                 if pickerNeeded == nil {
 8838 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8839 |                         draft: draft,
 8840 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8852:27: warning: no 'async' operations occur within 'await' expression
 8850 |                     await completionGate.value
 8851 |                     try Task.checkCancellation()
 8852 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8853 |                         return
 8854 |                     }

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8859:20: warning: no 'async' operations occur within 'await' expression
 8857 |                 if let cursorUTF8Offset,
 8858 |                    requestCompletion,
 8859 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8860 |                        parse: parse,
 8861 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:8865:37: warning: no 'async' operations occur within 'await' expression
 8863 |                    ) == true
 8864 |                 {
 8865 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8866 |                         parse: parse,
 8867 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/CapturePanelModel.swift:9094:28: warning: no 'async' operations occur within 'await' expression
 9092 |         Task { [weak self, processClient] in
 9093 |             do {
 9094 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 9095 |                 let processClientIdentity = processClient.identityToken
 9096 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[185/196] Compiling BobMacCapture RefsActionsMenu.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[186/196] Compiling BobMacCapture RefsAnnotationImages.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[187/196] Compiling BobMacCapture RefsCopyCardView.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[188/196] Compiling BobMacCapture RefsCopyHUD.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[189/196] Compiling BobMacCapture RefsFooter.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[190/196] Compiling BobMacCapture RefsInspectorImageViews.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[191/196] Compiling BobMacCapture RefsInspectorLoader.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[192/196] Compiling BobMacCapture RefsInspectorScroll.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[193/196] Compiling BobMacCapture RefsInspectorView.swift
/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-argv-pQtZiugWXv/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[193/196] Write Objects.LinkFileList
[194/196] Linking BobMacCapture
[195/196] Applying BobMacCapture
Build complete! (108.05s)
PASS BobMacCaptureTests
PASS BobMacCaptureInstallHelperTests
PASS CaptureCoreTests
PASS RefsCoreTests
Type-check only: macOS test targets were checked against a stub; CI still runs the tests.
succeeded  exit=0  duration=323783ms

