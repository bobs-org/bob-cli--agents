# Chat History - ace-run (bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2--mon-0)

- **TIMESTAMP:** 2026-10-26 13:44:21 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.2--mon-0

## Prompt

sase monitor start --command 'bash /tmp/bob_mac_scratch_check.sh' --reason 'Compile the approved bob-mac-capture changes on macOS in a disposable scratch copy'

## Response

sase tool run 81621a37d31a461864bb86d8e946597a
X11 forwarding request failed on channel 0
MAC_SCRATCH=/tmp/bob-mac-capture-check.3Q9EC7
X11 forwarding request failed on channel 0
Building for production...
[0/6] Write sources
[3/6] Write swift-version--1AB21518FC5DEDBE.txt
[5/7] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?
[6/8] Compiling RefsCore HighlightsSaveScan.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
948 |     }
949 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
948 |     }
949 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:82:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 80 |     NSApplication.shared.addSceneRepresentation(representation)
 81 |     settingsSceneRepresentation = representation
 82 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 83 |       representation.environment.openSettings()
 84 |     }
    :
942 |   var activateApplication: () -> Void
943 | 
944 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:292:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
290 |     menu.addItem(redo)
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
294 |     menu.addItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:293:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
294 |     menu.addItem(
295 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:302:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
300 |     )
301 |     menu.addItem(
302 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
303 |     return menu
304 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:499:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
497 |   /// off MainActor state.
498 |   nonisolated static func storedHighlightsAppPath() -> String {
499 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
500 |   }
501 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:579:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
577 |       library: library,
578 |       opener: WorkspaceRefsOpener(),
579 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
580 |       tabs: tabsSession,
581 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:853:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
851 |       return
852 |     }
853 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
854 |   }
855 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:225:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
223 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
224 |     static let refsHighlightsCopyKey = "refsHighlightsCopyKey"
225 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
226 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
227 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:2070:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2068 |         }
2069 |         if let textView = firstResponder as? NSTextView,
2070 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2071 |            field.accessibilityIdentifier() == identifier
2072 |         {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:8177:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8175 |         newName: String
 8176 |     ) {
 8177 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8178 |               let rename = current.rename,
 8179 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11085:23: warning: no 'async' operations occur within 'await' expression
11083 |                 }
11084 | 
11085 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11086 |                     return
11087 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11090:21: warning: no 'async' operations occur within 'await' expression
11088 | 
11089 |                 if pickerNeeded == nil {
11090 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11091 |                         draft: draft,
11092 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11104:27: warning: no 'async' operations occur within 'await' expression
11102 |                     await completionGate.value
11103 |                     try Task.checkCancellation()
11104 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11105 |                         return
11106 |                     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11111:20: warning: no 'async' operations occur within 'await' expression
11109 |                 if let cursorUTF8Offset,
11110 |                    requestCompletion,
11111 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11112 |                        parse: parse,
11113 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11117:37: warning: no 'async' operations occur within 'await' expression
11115 |                    ) == true
11116 |                 {
11117 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11118 |                         parse: parse,
11119 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11346:28: warning: no 'async' operations occur within 'await' expression
11344 |         Task { [weak self, processClient] in
11345 |             do {
11346 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
11347 |                 let processClientIdentity = processClient.identityToken
11348 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2330:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
2330 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2331 |     }
2332 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2329:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2327 |         }
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2330 |             + Text(String(label[range.upperBound...]))
2331 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:21: note: static property declared here
 170 | 
 171 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 173 | 
 174 |   private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:673:21: warning: expression of type 'Bool' is unused [#no-usage]
 671 |   private func refreshSnapshotAfterRename() async {
 672 |     while let current = snapshotTask {
 673 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 674 |     }
 675 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:677:21: warning: expression of type 'Bool' is unused [#no-usage]
 675 |     refreshSnapshot(reason: .manual)
 676 |     while let current = snapshotTask {
 677 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 678 |     }
 679 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:945:21: warning: expression of type 'Bool' is unused [#no-usage]
 943 |   private func runPostScanRefresh() async {
 944 |     while let current = snapshotTask {
 945 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 946 |       if snapshotTask == nil {
 947 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:952:21: warning: expression of type 'Bool' is unused [#no-usage]
 950 |     refresh(reason: .scan)
 951 |     while let current = snapshotTask {
 952 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 953 |       if snapshotTask == nil {
 954 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:1018:16: warning: no 'async' operations occur within 'await' expression
1016 |       },
1017 |       onFailure: { [weak self] message in
1018 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
1019 |       }
1020 |     )

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:310:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |         // rows report nil, which never clears the current rect.
309 |         .onGeometryChange(for: CGRect?.self) { proxy in
310 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |             ? proxy.frame(in: .named("refsPanel")) : nil
312 |         } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:358:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |       .transition(removalTransition)
357 |       .onGeometryChange(for: CGRect?.self) { proxy in
358 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |           ? proxy.frame(in: .named("refsPanel")) : nil
360 |       } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:230:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 228 |     completion: @escaping (Error?) -> Void
 229 |   ) {
 230 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 231 |     configuration.activates = true
 232 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:279:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 277 | 
 278 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 279 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 280 |     configuration.activates = true
 281 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:771:14: warning: no 'async' operations occur within 'await' expression
 769 |     }.store(in: &subscriptions)
 770 |     library.$refreshState.sink { [weak self] _ in
 771 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 772 |     }.store(in: &subscriptions)
 773 |     library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3564:7: warning: result of call to 'openSelected' is unused [#no-usage]
3562 |       openWithDefaultApp(item)
3563 |     case .note, .reveal, .task:
3564 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3565 |     }
3566 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3601:9: warning: no 'async' operations occur within 'await' expression
3599 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3600 |       Task {
3601 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3602 |       }
3603 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3628:9: warning: no 'async' operations occur within 'await' expression
3626 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3627 |       Task {
3628 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3629 |       }
3630 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3686:9: warning: no 'async' operations occur within 'await' expression
3684 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3685 |       Task {
3686 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3687 |           itemID: item.id,
3688 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3717:9: warning: no 'async' operations occur within 'await' expression
3715 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3716 |       Task {
3717 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3718 |           itemID: item.id,
3719 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
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
Build of product 'BobMacCapture' complete! (179.91s)
/tmp/bob-mac-capture-check.3Q9EC7/.build/bundle/Bob Mac Capture.app/Contents/MacOS/BobMacCapture: replacing existing signature
/tmp/bob-mac-capture-check.3Q9EC7/.build/bundle/Bob Mac Capture.app: replacing existing signature
/tmp/bob-mac-capture-check.3Q9EC7/.build/bundle/Bob Mac Capture.app
BUNDLE_STATUS=0
X11 forwarding request failed on channel 0
./Scripts/typecheck-tests.sh
Building for debugging...
[0/18] Write sources
[5/18] Write refs-rank-entitlement.plist
[5/18] Write BobMacCaptureInstallHelper-entitlement.plist
[7/18] Write BobMacCapture-entitlement.plist
[8/18] Write swift-version--1AB21518FC5DEDBE.txt
[10/78] Emitting module CaptureCore
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?
[11/86] Compiling CaptureCore CaptureRelationshipCopy.swift
[12/86] Compiling CaptureCore CaptureRelationshipPresentation.swift
[13/86] Compiling CaptureCore CaptureSavedTemplates.swift
[14/86] Compiling CaptureCore CaptureSubBulletPresentation.swift
[15/86] Compiling CaptureCore CaptureSuccessorPresentation.swift
[16/86] Compiling CaptureCore CaptureTargetsCache.swift
[17/86] Compiling CaptureCore CaptureTaskBlockPresentation.swift
[18/86] Compiling CaptureCore CaptureTaskCompletePresentation.swift
[19/86] Compiling CaptureCore CapturePanelPlacement.swift
[20/86] Compiling CaptureCore CapturePickerHelpers.swift
[21/86] Compiling CaptureCore CapturePickerPresentation.swift
[22/86] Compiling CaptureCore CapturePlanBudgetPresentation.swift
[23/86] Compiling CaptureCore CapturePomodoroAdjustPresentation.swift
[24/86] Compiling CaptureCore CapturePomodoroBlockPresentation.swift
[25/86] Compiling CaptureCore CapturePomodoroClosePresentation.swift
[26/86] Compiling CaptureCore CapturePomodoroLineTokens.swift
[27/86] Compiling CaptureCore CapturePomodoroLinkPresentation.swift
[28/86] Compiling CaptureCore CapturePomodoroResetPresentation.swift
[29/86] Compiling CaptureCore CapturePomodoroShiftPresentation.swift
[30/86] Compiling CaptureCore CapturePomodoroStartPresentation.swift
[31/86] Compiling CaptureCore CaptureProjectNotePresentation.swift
[32/86] Compiling CaptureCore CaptureRefFileUnder.swift
[33/86] Compiling CaptureCore CaptureRefPresentation.swift
[34/86] Compiling CaptureCore CaptureRelatedModels.swift
[35/86] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[36/86] Compiling CaptureCore BlockIDPickerIndex.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[37/86] Compiling CaptureCore BlockIDRules.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[38/86] Compiling CaptureCore BobEnvironment.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[39/86] Compiling CaptureCore BobErrors.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[40/86] Compiling CaptureCore BobExecutableResolver.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[41/86] Compiling CaptureCore BobMacCaptureLaunchContext.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[42/86] Compiling CaptureCore BobProcessClient.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[43/86] Compiling CaptureCore CanceledDraftStashStore.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[44/86] Compiling CaptureCore ParentTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?
[45/86] Compiling CaptureCore PomodoroHomes.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?
[46/86] Compiling CaptureCore SimilarTasksBandEdits.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?
[47/86] Compiling CaptureCore SimilarTasksBandPolicy.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?
[48/86] Compiling CaptureCore SimilarTasksBandPresentation.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?
[49/86] Compiling CaptureCore TaskCompletePickerPresentation.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?
[50/86] Compiling CaptureCore TaskDisplayText.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?
[51/86] Compiling CaptureCore TaskLinkPickerPresentation.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?
[52/86] Compiling CaptureCore CaptureAgendaFitPlanner.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[53/86] Compiling CaptureCore CaptureAgendaHold.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[54/86] Compiling CaptureCore CaptureAgendaInlineText.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[55/86] Compiling CaptureCore CaptureAgendaLayout.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[56/86] Compiling CaptureCore CaptureAgendaModels.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[57/86] Compiling CaptureCore CaptureAgendaPresentation.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[58/86] Compiling CaptureCore CaptureAgendaRefreshFilter.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[59/86] Compiling CaptureCore CaptureAgendaRefreshState.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[60/86] Compiling CaptureCore CaptureAgendaVisibility.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[61/86] Compiling CaptureCore CaptureTemplateStart.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?
[62/86] Compiling CaptureCore CaptureTextRanges.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?
[63/86] Compiling CaptureCore CaptureTodayPomodoroGoto.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?
[64/86] Compiling CaptureCore CaptureTogglePresentation.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?
[65/86] Compiling CaptureCore CompletionRowContent.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?
[66/86] Compiling CaptureCore DependencyPickerPresentation.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?
[67/86] Compiling CaptureCore FuzzyMatcher.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?
[68/86] Compiling CaptureCore ObsidianOpenURL.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/CaptureCore/CaptureModels.swift:6739:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6737 | }
6738 | 
6739 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6740 |   public let replacement: String
6741 |   public let route: String?
[69/86] Compiling CaptureCore CaptureBlockDiffRow.swift
[70/86] Compiling CaptureCore CaptureCloseTaskCommaAssist.swift
[71/86] Compiling CaptureCore CaptureCloseTaskCommaProvenance.swift
[72/86] Compiling CaptureCore CaptureEditWrite.swift
[73/86] Compiling CaptureCore CaptureInboxRoutePresentation.swift
[74/86] Compiling CaptureCore CaptureLinkGuardPresentation.swift
[75/86] Compiling CaptureCore CaptureModels.swift
[76/86] Compiling CaptureCore CaptureOpenHintPresentation.swift
[77/86] Compiling CaptureCore CaptureOpenPlan.swift
[78/120] Compiling RefsCore RefsStores.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[79/120] Compiling RefsCore RefsTabClose.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[80/120] Compiling RefsCore RefsTabsRanking.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[81/120] Compiling RefsCore RefsToday.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[82/124] Compiling RefsCore HighlightsSaveScan.swift
[83/124] Compiling RefsCore RefsArrivals.swift
[84/124] Compiling RefsCore RefsCaption.swift
[85/124] Compiling RefsCore RefsCode.swift
[86/124] Compiling RefsCore RefsModel.swift
[87/124] Compiling RefsCore RefsNew.swift
[88/124] Compiling RefsCore RefsNewest.swift
[89/124] Compiling RefsCore RefsPDFUpdates.swift
[90/124] Compiling RefsCore RefsScan.swift
[91/124] Compiling RefsCore RefsScanReceipt.swift
[92/124] Compiling RefsCore RefsSectionedWindow.swift
[93/124] Compiling RefsCore RefsSelection.swift
[94/124] Compiling RefsCore RefsPanelGeometry.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {
[95/124] Compiling RefsCore RefsQuoteUnderline.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {
[96/124] Compiling RefsCore RefsRanking.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {
[97/124] Compiling RefsCore RefsRename.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {
[98/124] Compiling RefsCore RefsHighlightsTabs.swift
[99/124] Compiling RefsCore RefsInspector.swift
[100/124] Compiling RefsCore RefsInspectorImages.swift
[101/124] Compiling RefsCore RefsListScroll.swift
[102/124] Compiling RefsCore RefsCopy.swift
[103/124] Compiling RefsCore RefsDecoding.swift
[104/124] Compiling RefsCore RefsFetching.swift
[105/124] Compiling RefsCore RefsHighlightPicker.swift
[106/124] Emitting module RefsCore
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[107/124] Compiling RefsCore RefsTodayLinkCard.swift
[108/124] Compiling RefsCore RefsTodayLinkModels.swift
[109/124] Compiling RefsCore RefsTodayLinkPresentation.swift
[110/124] Compiling RefsCore RefsWatcherRelevance.swift
[111/197] Emitting module refs_rank
[112/197] Compiling refs_rank main.swift
[112/197] Write Objects.LinkFileList
[113/197] Linking refs-rank
[114/197] Applying refs-rank
[116/197] Compiling BobMacCaptureInstallHelper InstallHelperError.swift
[117/197] Compiling BobMacCaptureInstallHelper InstallHelperArguments.swift
[118/197] Compiling BobMacCaptureInstallHelper BobMacCaptureInstallHelperMain.swift
[119/197] Compiling BobMacCaptureInstallHelper InstallRelauncher.swift
[120/197] Emitting module BobMacCaptureInstallHelper
[120/197] Write Objects.LinkFileList
[121/197] Linking BobMacCaptureInstallHelper
[122/197] Applying BobMacCaptureInstallHelper
[124/197] Emitting module BobMacCapture
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
948 |     }
949 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
948 |     }
949 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:225:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
223 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
224 |     static let refsHighlightsCopyKey = "refsHighlightsCopyKey"
225 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
226 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
227 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:21: note: static property declared here
 170 | 
 171 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 173 | 
 174 |   private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[125/206] Compiling BobMacCapture AccessibilityTrust.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
948 |     }
949 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
948 |     }
949 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:82:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 80 |     NSApplication.shared.addSceneRepresentation(representation)
 81 |     settingsSceneRepresentation = representation
 82 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 83 |       representation.environment.openSettings()
 84 |     }
    :
942 |   var activateApplication: () -> Void
943 | 
944 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:292:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
290 |     menu.addItem(redo)
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
294 |     menu.addItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:293:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
294 |     menu.addItem(
295 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:302:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
300 |     )
301 |     menu.addItem(
302 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
303 |     return menu
304 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:499:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
497 |   /// off MainActor state.
498 |   nonisolated static func storedHighlightsAppPath() -> String {
499 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
500 |   }
501 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:579:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
577 |       library: library,
578 |       opener: WorkspaceRefsOpener(),
579 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
580 |       tabs: tabsSession,
581 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:853:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
851 |       return
852 |     }
853 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
854 |   }
855 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:225:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
223 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
224 |     static let refsHighlightsCopyKey = "refsHighlightsCopyKey"
225 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
226 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
227 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[126/206] Compiling BobMacCapture AppDelegate.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
948 |     }
949 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
948 |     }
949 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:82:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 80 |     NSApplication.shared.addSceneRepresentation(representation)
 81 |     settingsSceneRepresentation = representation
 82 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 83 |       representation.environment.openSettings()
 84 |     }
    :
942 |   var activateApplication: () -> Void
943 | 
944 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:292:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
290 |     menu.addItem(redo)
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
294 |     menu.addItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:293:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
294 |     menu.addItem(
295 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:302:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
300 |     )
301 |     menu.addItem(
302 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
303 |     return menu
304 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:499:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
497 |   /// off MainActor state.
498 |   nonisolated static func storedHighlightsAppPath() -> String {
499 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
500 |   }
501 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:579:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
577 |       library: library,
578 |       opener: WorkspaceRefsOpener(),
579 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
580 |       tabs: tabsSession,
581 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:853:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
851 |       return
852 |     }
853 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
854 |   }
855 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:225:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
223 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
224 |     static let refsHighlightsCopyKey = "refsHighlightsCopyKey"
225 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
226 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
227 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[127/206] Compiling BobMacCapture AppRelauncher.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
948 |     }
949 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
948 |     }
949 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:82:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 80 |     NSApplication.shared.addSceneRepresentation(representation)
 81 |     settingsSceneRepresentation = representation
 82 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 83 |       representation.environment.openSettings()
 84 |     }
    :
942 |   var activateApplication: () -> Void
943 | 
944 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:292:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
290 |     menu.addItem(redo)
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
294 |     menu.addItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:293:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
294 |     menu.addItem(
295 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:302:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
300 |     )
301 |     menu.addItem(
302 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
303 |     return menu
304 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:499:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
497 |   /// off MainActor state.
498 |   nonisolated static func storedHighlightsAppPath() -> String {
499 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
500 |   }
501 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:579:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
577 |       library: library,
578 |       opener: WorkspaceRefsOpener(),
579 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
580 |       tabs: tabsSession,
581 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:853:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
851 |       return
852 |     }
853 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
854 |   }
855 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:225:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
223 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
224 |     static let refsHighlightsCopyKey = "refsHighlightsCopyKey"
225 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
226 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
227 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[128/206] Compiling BobMacCapture AppSettings.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
948 |     }
949 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
948 |     }
949 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:82:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 80 |     NSApplication.shared.addSceneRepresentation(representation)
 81 |     settingsSceneRepresentation = representation
 82 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 83 |       representation.environment.openSettings()
 84 |     }
    :
942 |   var activateApplication: () -> Void
943 | 
944 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:292:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
290 |     menu.addItem(redo)
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
294 |     menu.addItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:293:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
294 |     menu.addItem(
295 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:302:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
300 |     )
301 |     menu.addItem(
302 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
303 |     return menu
304 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:499:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
497 |   /// off MainActor state.
498 |   nonisolated static func storedHighlightsAppPath() -> String {
499 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
500 |   }
501 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:579:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
577 |       library: library,
578 |       opener: WorkspaceRefsOpener(),
579 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
580 |       tabs: tabsSession,
581 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:853:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
851 |       return
852 |     }
853 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
854 |   }
855 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:225:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
223 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
224 |     static let refsHighlightsCopyKey = "refsHighlightsCopyKey"
225 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
226 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
227 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[129/206] Compiling BobMacCapture BlockDiffCard.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
948 |     }
949 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
948 |     }
949 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:82:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 80 |     NSApplication.shared.addSceneRepresentation(representation)
 81 |     settingsSceneRepresentation = representation
 82 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 83 |       representation.environment.openSettings()
 84 |     }
    :
942 |   var activateApplication: () -> Void
943 | 
944 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:292:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
290 |     menu.addItem(redo)
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
294 |     menu.addItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:293:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
294 |     menu.addItem(
295 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:302:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
300 |     )
301 |     menu.addItem(
302 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
303 |     return menu
304 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:499:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
497 |   /// off MainActor state.
498 |   nonisolated static func storedHighlightsAppPath() -> String {
499 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
500 |   }
501 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:579:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
577 |       library: library,
578 |       opener: WorkspaceRefsOpener(),
579 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
580 |       tabs: tabsSession,
581 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:853:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
851 |       return
852 |     }
853 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
854 |   }
855 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:225:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
223 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
224 |     static let refsHighlightsCopyKey = "refsHighlightsCopyKey"
225 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
226 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
227 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[130/206] Compiling BobMacCapture BlockIDField.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
948 |     }
949 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
948 |     }
949 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:82:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 80 |     NSApplication.shared.addSceneRepresentation(representation)
 81 |     settingsSceneRepresentation = representation
 82 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 83 |       representation.environment.openSettings()
 84 |     }
    :
942 |   var activateApplication: () -> Void
943 | 
944 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:292:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
290 |     menu.addItem(redo)
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
294 |     menu.addItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:293:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
294 |     menu.addItem(
295 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:302:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
300 |     )
301 |     menu.addItem(
302 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
303 |     return menu
304 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:499:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
497 |   /// off MainActor state.
498 |   nonisolated static func storedHighlightsAppPath() -> String {
499 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
500 |   }
501 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:579:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
577 |       library: library,
578 |       opener: WorkspaceRefsOpener(),
579 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
580 |       tabs: tabsSession,
581 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:853:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
851 |       return
852 |     }
853 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
854 |   }
855 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:225:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
223 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
224 |     static let refsHighlightsCopyKey = "refsHighlightsCopyKey"
225 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
226 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
227 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[131/206] Compiling BobMacCapture BobMacCaptureMain.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
948 |     }
949 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
948 |     }
949 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:82:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 80 |     NSApplication.shared.addSceneRepresentation(representation)
 81 |     settingsSceneRepresentation = representation
 82 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 83 |       representation.environment.openSettings()
 84 |     }
    :
942 |   var activateApplication: () -> Void
943 | 
944 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:292:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
290 |     menu.addItem(redo)
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
294 |     menu.addItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:293:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
294 |     menu.addItem(
295 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:302:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
300 |     )
301 |     menu.addItem(
302 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
303 |     return menu
304 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:499:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
497 |   /// off MainActor state.
498 |   nonisolated static func storedHighlightsAppPath() -> String {
499 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
500 |   }
501 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:579:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
577 |       library: library,
578 |       opener: WorkspaceRefsOpener(),
579 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
580 |       tabs: tabsSession,
581 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:853:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
851 |       return
852 |     }
853 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
854 |   }
855 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:225:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
223 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
224 |     static let refsHighlightsCopyKey = "refsHighlightsCopyKey"
225 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
226 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
227 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[132/206] Compiling BobMacCapture BobPanelCoordinator.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
948 |     }
949 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
948 |     }
949 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:82:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 80 |     NSApplication.shared.addSceneRepresentation(representation)
 81 |     settingsSceneRepresentation = representation
 82 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 83 |       representation.environment.openSettings()
 84 |     }
    :
942 |   var activateApplication: () -> Void
943 | 
944 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:292:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
290 |     menu.addItem(redo)
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
294 |     menu.addItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:293:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
294 |     menu.addItem(
295 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:302:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
300 |     )
301 |     menu.addItem(
302 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
303 |     return menu
304 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:499:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
497 |   /// off MainActor state.
498 |   nonisolated static func storedHighlightsAppPath() -> String {
499 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
500 |   }
501 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:579:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
577 |       library: library,
578 |       opener: WorkspaceRefsOpener(),
579 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
580 |       tabs: tabsSession,
581 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:853:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
851 |       return
852 |     }
853 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
854 |   }
855 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:225:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
223 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
224 |     static let refsHighlightsCopyKey = "refsHighlightsCopyKey"
225 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
226 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
227 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[133/206] Compiling BobMacCapture BundleSigningInspector.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
948 |     }
949 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
948 |     }
949 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:82:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 80 |     NSApplication.shared.addSceneRepresentation(representation)
 81 |     settingsSceneRepresentation = representation
 82 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 83 |       representation.environment.openSettings()
 84 |     }
    :
942 |   var activateApplication: () -> Void
943 | 
944 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:292:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
290 |     menu.addItem(redo)
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
294 |     menu.addItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:293:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
294 |     menu.addItem(
295 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:302:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
300 |     )
301 |     menu.addItem(
302 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
303 |     return menu
304 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:499:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
497 |   /// off MainActor state.
498 |   nonisolated static func storedHighlightsAppPath() -> String {
499 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
500 |   }
501 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:579:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
577 |       library: library,
578 |       opener: WorkspaceRefsOpener(),
579 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
580 |       tabs: tabsSession,
581 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:853:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
851 |       return
852 |     }
853 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
854 |   }
855 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:225:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
223 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
224 |     static let refsHighlightsCopyKey = "refsHighlightsCopyKey"
225 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
226 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
227 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[134/206] Compiling BobMacCapture CanceledDraftStash.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
948 |     }
949 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:947:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {
947 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
948 |     }
949 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:82:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 80 |     NSApplication.shared.addSceneRepresentation(representation)
 81 |     settingsSceneRepresentation = representation
 82 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 83 |       representation.environment.openSettings()
 84 |     }
    :
942 |   var activateApplication: () -> Void
943 | 
944 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
945 |     openSettings: @escaping () -> Void = {},
946 |     activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:292:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
290 |     menu.addItem(redo)
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
294 |     menu.addItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:293:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
291 |     menu.addItem(.separator())
292 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
293 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
294 |     menu.addItem(
295 |       NSMenuItem(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:302:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
300 |     )
301 |     menu.addItem(
302 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
303 |     return menu
304 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:499:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
497 |   /// off MainActor state.
498 |   nonisolated static func storedHighlightsAppPath() -> String {
499 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
500 |   }
501 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:579:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
577 |       library: library,
578 |       opener: WorkspaceRefsOpener(),
579 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
580 |       tabs: tabsSession,
581 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppDelegate.swift:853:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
851 |       return
852 |     }
853 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
854 |   }
855 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/AppSettings.swift:225:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
223 |     static let refsHighlightsTabsKey = "refsHighlightsTabsKey"
224 |     static let refsHighlightsCopyKey = "refsHighlightsCopyKey"
225 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
226 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
227 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[135/206] Compiling BobMacCapture RefsScanReceiptObserver.swift
[136/206] Compiling BobMacCapture RefsSearchBar.swift
[137/206] Compiling BobMacCapture RefsTabsViews.swift
[138/206] Compiling BobMacCapture RefsTodayLinkCardView.swift
[139/206] Compiling BobMacCapture RefsUnderlineRenderer.swift
[140/206] Compiling BobMacCapture RefsVisualTokens.swift
[141/206] Compiling BobMacCapture RefsHighlightsCopyKey.swift
[142/206] Compiling BobMacCapture RefsHighlightsOpenKey.swift
[143/206] Compiling BobMacCapture RefsHighlightsTabsKey.swift
[144/206] Compiling BobMacCapture RefsHotkeyRegistration.swift
[145/206] Compiling BobMacCapture HighlightsSaveKeyMonitor.swift
[146/206] Compiling BobMacCapture HighlightsTakeover.swift
[147/206] Compiling BobMacCapture HotKeyRegistry.swift
[148/206] Compiling BobMacCapture NotificationService.swift
[149/206] Compiling BobMacCapture PlainTextPaste.swift
[150/206] Compiling BobMacCapture PomodoroBlockView.swift
[151/206] Compiling BobMacCapture PomodoroHomeColor.swift
[152/206] Compiling BobMacCapture PomodoroNameField.swift
[153/206] Compiling BobMacCapture PomodoroThemeViews.swift
[154/206] Compiling BobMacCapture AXHighlightsTabsReader.swift
[155/206] Compiling BobMacCapture RelationLabelField.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[156/206] Compiling BobMacCapture SavedTemplateShelf.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[157/206] Compiling BobMacCapture SettingsView.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[158/206] Compiling BobMacCapture Signposts.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[159/206] Compiling BobMacCapture SimilarTasksBandView.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[160/206] Compiling BobMacCapture StatusItemController.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[161/206] Compiling BobMacCapture StatusItemGlyph.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[162/206] Compiling BobMacCapture TaskBlockView.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[163/206] Compiling BobMacCapture VaultTargetWatcher.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[164/206] Compiling BobMacCapture RefsActionsMenu.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[165/206] Compiling BobMacCapture RefsAnnotationImages.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[166/206] Compiling BobMacCapture RefsCodePreviewWell.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[167/206] Compiling BobMacCapture RefsCopyCardView.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[168/206] Compiling BobMacCapture RefsCopyHUD.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[169/206] Compiling BobMacCapture RefsFooter.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[170/206] Compiling BobMacCapture RefsInspectorImageViews.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[171/206] Compiling BobMacCapture RefsInspectorLoader.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[172/206] Compiling BobMacCapture RefsInspectorScroll.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[173/206] Compiling BobMacCapture RefsInspectorView.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[174/206] Compiling BobMacCapture CapturePanelWindowSizer.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:21: note: static property declared here
 170 | 
 171 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 173 | 
 174 |   private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[175/206] Compiling BobMacCapture CapturePickerFilterField.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:21: note: static property declared here
 170 | 
 171 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 173 | 
 174 |   private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[176/206] Compiling BobMacCapture CapturePickerState.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:21: note: static property declared here
 170 | 
 171 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 173 | 
 174 |   private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[177/206] Compiling BobMacCapture CapturePickerView.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:21: note: static property declared here
 170 | 
 171 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 173 | 
 174 |   private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[178/206] Compiling BobMacCapture CapturePlanBudgetMeterRow.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:21: note: static property declared here
 170 | 
 171 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 173 | 
 174 |   private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[179/206] Compiling BobMacCapture CapturePullInChoice.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:21: note: static property declared here
 170 | 
 171 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 173 | 
 174 |   private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[180/206] Compiling BobMacCapture CapturePullInChoiceView.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:21: note: static property declared here
 170 | 
 171 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 173 | 
 174 |   private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[181/206] Compiling BobMacCapture CaptureShowRefreshWindow.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:21: note: static property declared here
 170 | 
 171 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 173 | 
 174 |   private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[182/206] Compiling BobMacCapture CaptureSnippetResolver.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:21: note: static property declared here
 170 | 
 171 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 173 | 
 174 |   private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[183/206] Compiling BobMacCapture CaptureTargetsRefreshGate.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:21: note: static property declared here
 170 | 
 171 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 173 | 
 174 |   private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[184/206] Compiling BobMacCapture RefsKeyRouter.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:673:21: warning: expression of type 'Bool' is unused [#no-usage]
 671 |   private func refreshSnapshotAfterRename() async {
 672 |     while let current = snapshotTask {
 673 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 674 |     }
 675 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:677:21: warning: expression of type 'Bool' is unused [#no-usage]
 675 |     refreshSnapshot(reason: .manual)
 676 |     while let current = snapshotTask {
 677 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 678 |     }
 679 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:945:21: warning: expression of type 'Bool' is unused [#no-usage]
 943 |   private func runPostScanRefresh() async {
 944 |     while let current = snapshotTask {
 945 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 946 |       if snapshotTask == nil {
 947 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:952:21: warning: expression of type 'Bool' is unused [#no-usage]
 950 |     refresh(reason: .scan)
 951 |     while let current = snapshotTask {
 952 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 953 |       if snapshotTask == nil {
 954 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:1018:16: warning: no 'async' operations occur within 'await' expression
1016 |       },
1017 |       onFailure: { [weak self] message in
1018 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
1019 |       }
1020 |     )

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:310:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |         // rows report nil, which never clears the current rect.
309 |         .onGeometryChange(for: CGRect?.self) { proxy in
310 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |             ? proxy.frame(in: .named("refsPanel")) : nil
312 |         } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:358:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |       .transition(removalTransition)
357 |       .onGeometryChange(for: CGRect?.self) { proxy in
358 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |           ? proxy.frame(in: .named("refsPanel")) : nil
360 |       } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:230:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 228 |     completion: @escaping (Error?) -> Void
 229 |   ) {
 230 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 231 |     configuration.activates = true
 232 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:279:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 277 | 
 278 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 279 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 280 |     configuration.activates = true
 281 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:771:14: warning: no 'async' operations occur within 'await' expression
 769 |     }.store(in: &subscriptions)
 770 |     library.$refreshState.sink { [weak self] _ in
 771 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 772 |     }.store(in: &subscriptions)
 773 |     library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3564:7: warning: result of call to 'openSelected' is unused [#no-usage]
3562 |       openWithDefaultApp(item)
3563 |     case .note, .reveal, .task:
3564 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3565 |     }
3566 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3601:9: warning: no 'async' operations occur within 'await' expression
3599 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3600 |       Task {
3601 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3602 |       }
3603 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3628:9: warning: no 'async' operations occur within 'await' expression
3626 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3627 |       Task {
3628 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3629 |       }
3630 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3686:9: warning: no 'async' operations occur within 'await' expression
3684 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3685 |       Task {
3686 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3687 |           itemID: item.id,
3688 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3717:9: warning: no 'async' operations occur within 'await' expression
3715 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3716 |       Task {
3717 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3718 |           itemID: item.id,
3719 |           title: item.title.text,
[185/206] Compiling BobMacCapture RefsLibrary.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:673:21: warning: expression of type 'Bool' is unused [#no-usage]
 671 |   private func refreshSnapshotAfterRename() async {
 672 |     while let current = snapshotTask {
 673 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 674 |     }
 675 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:677:21: warning: expression of type 'Bool' is unused [#no-usage]
 675 |     refreshSnapshot(reason: .manual)
 676 |     while let current = snapshotTask {
 677 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 678 |     }
 679 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:945:21: warning: expression of type 'Bool' is unused [#no-usage]
 943 |   private func runPostScanRefresh() async {
 944 |     while let current = snapshotTask {
 945 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 946 |       if snapshotTask == nil {
 947 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:952:21: warning: expression of type 'Bool' is unused [#no-usage]
 950 |     refresh(reason: .scan)
 951 |     while let current = snapshotTask {
 952 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 953 |       if snapshotTask == nil {
 954 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:1018:16: warning: no 'async' operations occur within 'await' expression
1016 |       },
1017 |       onFailure: { [weak self] message in
1018 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
1019 |       }
1020 |     )

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:310:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |         // rows report nil, which never clears the current rect.
309 |         .onGeometryChange(for: CGRect?.self) { proxy in
310 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |             ? proxy.frame(in: .named("refsPanel")) : nil
312 |         } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:358:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |       .transition(removalTransition)
357 |       .onGeometryChange(for: CGRect?.self) { proxy in
358 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |           ? proxy.frame(in: .named("refsPanel")) : nil
360 |       } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:230:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 228 |     completion: @escaping (Error?) -> Void
 229 |   ) {
 230 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 231 |     configuration.activates = true
 232 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:279:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 277 | 
 278 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 279 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 280 |     configuration.activates = true
 281 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:771:14: warning: no 'async' operations occur within 'await' expression
 769 |     }.store(in: &subscriptions)
 770 |     library.$refreshState.sink { [weak self] _ in
 771 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 772 |     }.store(in: &subscriptions)
 773 |     library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3564:7: warning: result of call to 'openSelected' is unused [#no-usage]
3562 |       openWithDefaultApp(item)
3563 |     case .note, .reveal, .task:
3564 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3565 |     }
3566 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3601:9: warning: no 'async' operations occur within 'await' expression
3599 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3600 |       Task {
3601 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3602 |       }
3603 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3628:9: warning: no 'async' operations occur within 'await' expression
3626 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3627 |       Task {
3628 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3629 |       }
3630 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3686:9: warning: no 'async' operations occur within 'await' expression
3684 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3685 |       Task {
3686 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3687 |           itemID: item.id,
3688 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3717:9: warning: no 'async' operations occur within 'await' expression
3715 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3716 |       Task {
3717 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3718 |           itemID: item.id,
3719 |           title: item.title.text,
[186/206] Compiling BobMacCapture RefsListView.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:673:21: warning: expression of type 'Bool' is unused [#no-usage]
 671 |   private func refreshSnapshotAfterRename() async {
 672 |     while let current = snapshotTask {
 673 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 674 |     }
 675 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:677:21: warning: expression of type 'Bool' is unused [#no-usage]
 675 |     refreshSnapshot(reason: .manual)
 676 |     while let current = snapshotTask {
 677 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 678 |     }
 679 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:945:21: warning: expression of type 'Bool' is unused [#no-usage]
 943 |   private func runPostScanRefresh() async {
 944 |     while let current = snapshotTask {
 945 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 946 |       if snapshotTask == nil {
 947 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:952:21: warning: expression of type 'Bool' is unused [#no-usage]
 950 |     refresh(reason: .scan)
 951 |     while let current = snapshotTask {
 952 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 953 |       if snapshotTask == nil {
 954 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:1018:16: warning: no 'async' operations occur within 'await' expression
1016 |       },
1017 |       onFailure: { [weak self] message in
1018 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
1019 |       }
1020 |     )

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:310:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |         // rows report nil, which never clears the current rect.
309 |         .onGeometryChange(for: CGRect?.self) { proxy in
310 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |             ? proxy.frame(in: .named("refsPanel")) : nil
312 |         } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:358:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |       .transition(removalTransition)
357 |       .onGeometryChange(for: CGRect?.self) { proxy in
358 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |           ? proxy.frame(in: .named("refsPanel")) : nil
360 |       } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:230:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 228 |     completion: @escaping (Error?) -> Void
 229 |   ) {
 230 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 231 |     configuration.activates = true
 232 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:279:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 277 | 
 278 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 279 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 280 |     configuration.activates = true
 281 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:771:14: warning: no 'async' operations occur within 'await' expression
 769 |     }.store(in: &subscriptions)
 770 |     library.$refreshState.sink { [weak self] _ in
 771 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 772 |     }.store(in: &subscriptions)
 773 |     library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3564:7: warning: result of call to 'openSelected' is unused [#no-usage]
3562 |       openWithDefaultApp(item)
3563 |     case .note, .reveal, .task:
3564 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3565 |     }
3566 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3601:9: warning: no 'async' operations occur within 'await' expression
3599 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3600 |       Task {
3601 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3602 |       }
3603 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3628:9: warning: no 'async' operations occur within 'await' expression
3626 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3627 |       Task {
3628 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3629 |       }
3630 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3686:9: warning: no 'async' operations occur within 'await' expression
3684 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3685 |       Task {
3686 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3687 |           itemID: item.id,
3688 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3717:9: warning: no 'async' operations occur within 'await' expression
3715 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3716 |       Task {
3717 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3718 |           itemID: item.id,
3719 |           title: item.title.text,
[187/206] Compiling BobMacCapture RefsPanel.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:673:21: warning: expression of type 'Bool' is unused [#no-usage]
 671 |   private func refreshSnapshotAfterRename() async {
 672 |     while let current = snapshotTask {
 673 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 674 |     }
 675 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:677:21: warning: expression of type 'Bool' is unused [#no-usage]
 675 |     refreshSnapshot(reason: .manual)
 676 |     while let current = snapshotTask {
 677 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 678 |     }
 679 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:945:21: warning: expression of type 'Bool' is unused [#no-usage]
 943 |   private func runPostScanRefresh() async {
 944 |     while let current = snapshotTask {
 945 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 946 |       if snapshotTask == nil {
 947 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:952:21: warning: expression of type 'Bool' is unused [#no-usage]
 950 |     refresh(reason: .scan)
 951 |     while let current = snapshotTask {
 952 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 953 |       if snapshotTask == nil {
 954 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:1018:16: warning: no 'async' operations occur within 'await' expression
1016 |       },
1017 |       onFailure: { [weak self] message in
1018 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
1019 |       }
1020 |     )

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:310:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |         // rows report nil, which never clears the current rect.
309 |         .onGeometryChange(for: CGRect?.self) { proxy in
310 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |             ? proxy.frame(in: .named("refsPanel")) : nil
312 |         } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:358:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |       .transition(removalTransition)
357 |       .onGeometryChange(for: CGRect?.self) { proxy in
358 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |           ? proxy.frame(in: .named("refsPanel")) : nil
360 |       } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:230:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 228 |     completion: @escaping (Error?) -> Void
 229 |   ) {
 230 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 231 |     configuration.activates = true
 232 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:279:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 277 | 
 278 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 279 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 280 |     configuration.activates = true
 281 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:771:14: warning: no 'async' operations occur within 'await' expression
 769 |     }.store(in: &subscriptions)
 770 |     library.$refreshState.sink { [weak self] _ in
 771 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 772 |     }.store(in: &subscriptions)
 773 |     library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3564:7: warning: result of call to 'openSelected' is unused [#no-usage]
3562 |       openWithDefaultApp(item)
3563 |     case .note, .reveal, .task:
3564 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3565 |     }
3566 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3601:9: warning: no 'async' operations occur within 'await' expression
3599 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3600 |       Task {
3601 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3602 |       }
3603 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3628:9: warning: no 'async' operations occur within 'await' expression
3626 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3627 |       Task {
3628 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3629 |       }
3630 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3686:9: warning: no 'async' operations occur within 'await' expression
3684 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3685 |       Task {
3686 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3687 |           itemID: item.id,
3688 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3717:9: warning: no 'async' operations occur within 'await' expression
3715 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3716 |       Task {
3717 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3718 |           itemID: item.id,
3719 |           title: item.title.text,
[188/206] Compiling BobMacCapture RefsPanelModel.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:673:21: warning: expression of type 'Bool' is unused [#no-usage]
 671 |   private func refreshSnapshotAfterRename() async {
 672 |     while let current = snapshotTask {
 673 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 674 |     }
 675 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:677:21: warning: expression of type 'Bool' is unused [#no-usage]
 675 |     refreshSnapshot(reason: .manual)
 676 |     while let current = snapshotTask {
 677 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 678 |     }
 679 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:945:21: warning: expression of type 'Bool' is unused [#no-usage]
 943 |   private func runPostScanRefresh() async {
 944 |     while let current = snapshotTask {
 945 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 946 |       if snapshotTask == nil {
 947 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:952:21: warning: expression of type 'Bool' is unused [#no-usage]
 950 |     refresh(reason: .scan)
 951 |     while let current = snapshotTask {
 952 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 953 |       if snapshotTask == nil {
 954 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:1018:16: warning: no 'async' operations occur within 'await' expression
1016 |       },
1017 |       onFailure: { [weak self] message in
1018 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
1019 |       }
1020 |     )

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:310:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |         // rows report nil, which never clears the current rect.
309 |         .onGeometryChange(for: CGRect?.self) { proxy in
310 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |             ? proxy.frame(in: .named("refsPanel")) : nil
312 |         } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:358:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |       .transition(removalTransition)
357 |       .onGeometryChange(for: CGRect?.self) { proxy in
358 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |           ? proxy.frame(in: .named("refsPanel")) : nil
360 |       } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:230:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 228 |     completion: @escaping (Error?) -> Void
 229 |   ) {
 230 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 231 |     configuration.activates = true
 232 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:279:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 277 | 
 278 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 279 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 280 |     configuration.activates = true
 281 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:771:14: warning: no 'async' operations occur within 'await' expression
 769 |     }.store(in: &subscriptions)
 770 |     library.$refreshState.sink { [weak self] _ in
 771 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 772 |     }.store(in: &subscriptions)
 773 |     library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3564:7: warning: result of call to 'openSelected' is unused [#no-usage]
3562 |       openWithDefaultApp(item)
3563 |     case .note, .reveal, .task:
3564 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3565 |     }
3566 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3601:9: warning: no 'async' operations occur within 'await' expression
3599 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3600 |       Task {
3601 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3602 |       }
3603 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3628:9: warning: no 'async' operations occur within 'await' expression
3626 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3627 |       Task {
3628 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3629 |       }
3630 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3686:9: warning: no 'async' operations occur within 'await' expression
3684 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3685 |       Task {
3686 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3687 |           itemID: item.id,
3688 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3717:9: warning: no 'async' operations occur within 'await' expression
3715 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3716 |       Task {
3717 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3718 |           itemID: item.id,
3719 |           title: item.title.text,
[189/206] Compiling BobMacCapture RefsPanelStates.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:673:21: warning: expression of type 'Bool' is unused [#no-usage]
 671 |   private func refreshSnapshotAfterRename() async {
 672 |     while let current = snapshotTask {
 673 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 674 |     }
 675 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:677:21: warning: expression of type 'Bool' is unused [#no-usage]
 675 |     refreshSnapshot(reason: .manual)
 676 |     while let current = snapshotTask {
 677 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 678 |     }
 679 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:945:21: warning: expression of type 'Bool' is unused [#no-usage]
 943 |   private func runPostScanRefresh() async {
 944 |     while let current = snapshotTask {
 945 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 946 |       if snapshotTask == nil {
 947 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:952:21: warning: expression of type 'Bool' is unused [#no-usage]
 950 |     refresh(reason: .scan)
 951 |     while let current = snapshotTask {
 952 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 953 |       if snapshotTask == nil {
 954 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:1018:16: warning: no 'async' operations occur within 'await' expression
1016 |       },
1017 |       onFailure: { [weak self] message in
1018 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
1019 |       }
1020 |     )

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:310:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |         // rows report nil, which never clears the current rect.
309 |         .onGeometryChange(for: CGRect?.self) { proxy in
310 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |             ? proxy.frame(in: .named("refsPanel")) : nil
312 |         } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:358:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |       .transition(removalTransition)
357 |       .onGeometryChange(for: CGRect?.self) { proxy in
358 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |           ? proxy.frame(in: .named("refsPanel")) : nil
360 |       } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:230:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 228 |     completion: @escaping (Error?) -> Void
 229 |   ) {
 230 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 231 |     configuration.activates = true
 232 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:279:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 277 | 
 278 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 279 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 280 |     configuration.activates = true
 281 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:771:14: warning: no 'async' operations occur within 'await' expression
 769 |     }.store(in: &subscriptions)
 770 |     library.$refreshState.sink { [weak self] _ in
 771 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 772 |     }.store(in: &subscriptions)
 773 |     library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3564:7: warning: result of call to 'openSelected' is unused [#no-usage]
3562 |       openWithDefaultApp(item)
3563 |     case .note, .reveal, .task:
3564 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3565 |     }
3566 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3601:9: warning: no 'async' operations occur within 'await' expression
3599 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3600 |       Task {
3601 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3602 |       }
3603 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3628:9: warning: no 'async' operations occur within 'await' expression
3626 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3627 |       Task {
3628 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3629 |       }
3630 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3686:9: warning: no 'async' operations occur within 'await' expression
3684 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3685 |       Task {
3686 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3687 |           itemID: item.id,
3688 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3717:9: warning: no 'async' operations occur within 'await' expression
3715 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3716 |       Task {
3717 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3718 |           itemID: item.id,
3719 |           title: item.title.text,
[190/206] Compiling BobMacCapture RefsPanelView.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:673:21: warning: expression of type 'Bool' is unused [#no-usage]
 671 |   private func refreshSnapshotAfterRename() async {
 672 |     while let current = snapshotTask {
 673 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 674 |     }
 675 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:677:21: warning: expression of type 'Bool' is unused [#no-usage]
 675 |     refreshSnapshot(reason: .manual)
 676 |     while let current = snapshotTask {
 677 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 678 |     }
 679 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:945:21: warning: expression of type 'Bool' is unused [#no-usage]
 943 |   private func runPostScanRefresh() async {
 944 |     while let current = snapshotTask {
 945 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 946 |       if snapshotTask == nil {
 947 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:952:21: warning: expression of type 'Bool' is unused [#no-usage]
 950 |     refresh(reason: .scan)
 951 |     while let current = snapshotTask {
 952 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 953 |       if snapshotTask == nil {
 954 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:1018:16: warning: no 'async' operations occur within 'await' expression
1016 |       },
1017 |       onFailure: { [weak self] message in
1018 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
1019 |       }
1020 |     )

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:310:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |         // rows report nil, which never clears the current rect.
309 |         .onGeometryChange(for: CGRect?.self) { proxy in
310 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |             ? proxy.frame(in: .named("refsPanel")) : nil
312 |         } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:358:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |       .transition(removalTransition)
357 |       .onGeometryChange(for: CGRect?.self) { proxy in
358 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |           ? proxy.frame(in: .named("refsPanel")) : nil
360 |       } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:230:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 228 |     completion: @escaping (Error?) -> Void
 229 |   ) {
 230 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 231 |     configuration.activates = true
 232 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:279:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 277 | 
 278 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 279 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 280 |     configuration.activates = true
 281 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:771:14: warning: no 'async' operations occur within 'await' expression
 769 |     }.store(in: &subscriptions)
 770 |     library.$refreshState.sink { [weak self] _ in
 771 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 772 |     }.store(in: &subscriptions)
 773 |     library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3564:7: warning: result of call to 'openSelected' is unused [#no-usage]
3562 |       openWithDefaultApp(item)
3563 |     case .note, .reveal, .task:
3564 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3565 |     }
3566 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3601:9: warning: no 'async' operations occur within 'await' expression
3599 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3600 |       Task {
3601 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3602 |       }
3603 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3628:9: warning: no 'async' operations occur within 'await' expression
3626 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3627 |       Task {
3628 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3629 |       }
3630 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3686:9: warning: no 'async' operations occur within 'await' expression
3684 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3685 |       Task {
3686 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3687 |           itemID: item.id,
3688 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3717:9: warning: no 'async' operations occur within 'await' expression
3715 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3716 |       Task {
3717 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3718 |           itemID: item.id,
3719 |           title: item.title.text,
[191/206] Compiling BobMacCapture RefsQuoteText.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:673:21: warning: expression of type 'Bool' is unused [#no-usage]
 671 |   private func refreshSnapshotAfterRename() async {
 672 |     while let current = snapshotTask {
 673 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 674 |     }
 675 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:677:21: warning: expression of type 'Bool' is unused [#no-usage]
 675 |     refreshSnapshot(reason: .manual)
 676 |     while let current = snapshotTask {
 677 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 678 |     }
 679 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:945:21: warning: expression of type 'Bool' is unused [#no-usage]
 943 |   private func runPostScanRefresh() async {
 944 |     while let current = snapshotTask {
 945 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 946 |       if snapshotTask == nil {
 947 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:952:21: warning: expression of type 'Bool' is unused [#no-usage]
 950 |     refresh(reason: .scan)
 951 |     while let current = snapshotTask {
 952 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 953 |       if snapshotTask == nil {
 954 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:1018:16: warning: no 'async' operations occur within 'await' expression
1016 |       },
1017 |       onFailure: { [weak self] message in
1018 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
1019 |       }
1020 |     )

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:310:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |         // rows report nil, which never clears the current rect.
309 |         .onGeometryChange(for: CGRect?.self) { proxy in
310 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |             ? proxy.frame(in: .named("refsPanel")) : nil
312 |         } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:358:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |       .transition(removalTransition)
357 |       .onGeometryChange(for: CGRect?.self) { proxy in
358 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |           ? proxy.frame(in: .named("refsPanel")) : nil
360 |       } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:230:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 228 |     completion: @escaping (Error?) -> Void
 229 |   ) {
 230 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 231 |     configuration.activates = true
 232 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:279:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 277 | 
 278 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 279 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 280 |     configuration.activates = true
 281 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:771:14: warning: no 'async' operations occur within 'await' expression
 769 |     }.store(in: &subscriptions)
 770 |     library.$refreshState.sink { [weak self] _ in
 771 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 772 |     }.store(in: &subscriptions)
 773 |     library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3564:7: warning: result of call to 'openSelected' is unused [#no-usage]
3562 |       openWithDefaultApp(item)
3563 |     case .note, .reveal, .task:
3564 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3565 |     }
3566 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3601:9: warning: no 'async' operations occur within 'await' expression
3599 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3600 |       Task {
3601 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3602 |       }
3603 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3628:9: warning: no 'async' operations occur within 'await' expression
3626 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3627 |       Task {
3628 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3629 |       }
3630 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3686:9: warning: no 'async' operations occur within 'await' expression
3684 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3685 |       Task {
3686 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3687 |           itemID: item.id,
3688 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3717:9: warning: no 'async' operations occur within 'await' expression
3715 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3716 |       Task {
3717 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3718 |           itemID: item.id,
3719 |           title: item.title.text,
[192/206] Compiling BobMacCapture RefsRenameCardView.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:673:21: warning: expression of type 'Bool' is unused [#no-usage]
 671 |   private func refreshSnapshotAfterRename() async {
 672 |     while let current = snapshotTask {
 673 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 674 |     }
 675 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:677:21: warning: expression of type 'Bool' is unused [#no-usage]
 675 |     refreshSnapshot(reason: .manual)
 676 |     while let current = snapshotTask {
 677 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 678 |     }
 679 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:945:21: warning: expression of type 'Bool' is unused [#no-usage]
 943 |   private func runPostScanRefresh() async {
 944 |     while let current = snapshotTask {
 945 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 946 |       if snapshotTask == nil {
 947 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:952:21: warning: expression of type 'Bool' is unused [#no-usage]
 950 |     refresh(reason: .scan)
 951 |     while let current = snapshotTask {
 952 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 953 |       if snapshotTask == nil {
 954 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:1018:16: warning: no 'async' operations occur within 'await' expression
1016 |       },
1017 |       onFailure: { [weak self] message in
1018 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
1019 |       }
1020 |     )

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:310:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |         // rows report nil, which never clears the current rect.
309 |         .onGeometryChange(for: CGRect?.self) { proxy in
310 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |             ? proxy.frame(in: .named("refsPanel")) : nil
312 |         } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:358:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |       .transition(removalTransition)
357 |       .onGeometryChange(for: CGRect?.self) { proxy in
358 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |           ? proxy.frame(in: .named("refsPanel")) : nil
360 |       } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:230:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 228 |     completion: @escaping (Error?) -> Void
 229 |   ) {
 230 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 231 |     configuration.activates = true
 232 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:279:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 277 | 
 278 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 279 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 280 |     configuration.activates = true
 281 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:771:14: warning: no 'async' operations occur within 'await' expression
 769 |     }.store(in: &subscriptions)
 770 |     library.$refreshState.sink { [weak self] _ in
 771 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 772 |     }.store(in: &subscriptions)
 773 |     library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3564:7: warning: result of call to 'openSelected' is unused [#no-usage]
3562 |       openWithDefaultApp(item)
3563 |     case .note, .reveal, .task:
3564 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3565 |     }
3566 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3601:9: warning: no 'async' operations occur within 'await' expression
3599 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3600 |       Task {
3601 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3602 |       }
3603 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3628:9: warning: no 'async' operations occur within 'await' expression
3626 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3627 |       Task {
3628 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3629 |       }
3630 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3686:9: warning: no 'async' operations occur within 'await' expression
3684 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3685 |       Task {
3686 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3687 |           itemID: item.id,
3688 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3717:9: warning: no 'async' operations occur within 'await' expression
3715 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3716 |       Task {
3717 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3718 |           itemID: item.id,
3719 |           title: item.title.text,
[193/206] Compiling BobMacCapture RefsRowView.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:673:21: warning: expression of type 'Bool' is unused [#no-usage]
 671 |   private func refreshSnapshotAfterRename() async {
 672 |     while let current = snapshotTask {
 673 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 674 |     }
 675 |     refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:677:21: warning: expression of type 'Bool' is unused [#no-usage]
 675 |     refreshSnapshot(reason: .manual)
 676 |     while let current = snapshotTask {
 677 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 678 |     }
 679 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:945:21: warning: expression of type 'Bool' is unused [#no-usage]
 943 |   private func runPostScanRefresh() async {
 944 |     while let current = snapshotTask {
 945 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 946 |       if snapshotTask == nil {
 947 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:952:21: warning: expression of type 'Bool' is unused [#no-usage]
 950 |     refresh(reason: .scan)
 951 |     while let current = snapshotTask {
 952 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 953 |       if snapshotTask == nil {
 954 |         break

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:1018:16: warning: no 'async' operations occur within 'await' expression
1016 |       },
1017 |       onFailure: { [weak self] message in
1018 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
1019 |       }
1020 |     )

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:310:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |         // rows report nil, which never clears the current rect.
309 |         .onGeometryChange(for: CGRect?.self) { proxy in
310 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |             ? proxy.frame(in: .named("refsPanel")) : nil
312 |         } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsListView.swift:358:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |       .transition(removalTransition)
357 |       .onGeometryChange(for: CGRect?.self) { proxy in
358 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |           ? proxy.frame(in: .named("refsPanel")) : nil
360 |       } action: { rect in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:394:38: note: property declared here
 392 |     return tabsFilter && tabsListing?.tabs[id] != nil
 393 |   }
 394 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 395 |     didSet {
 396 |       if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:230:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 228 |     completion: @escaping (Error?) -> Void
 229 |   ) {
 230 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 231 |     configuration.activates = true
 232 |     NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:279:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 277 | 
 278 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 279 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 280 |     configuration.activates = true
 281 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:771:14: warning: no 'async' operations occur within 'await' expression
 769 |     }.store(in: &subscriptions)
 770 |     library.$refreshState.sink { [weak self] _ in
 771 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 772 |     }.store(in: &subscriptions)
 773 |     library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3564:7: warning: result of call to 'openSelected' is unused [#no-usage]
3562 |       openWithDefaultApp(item)
3563 |     case .note, .reveal, .task:
3564 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3565 |     }
3566 |   }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3601:9: warning: no 'async' operations occur within 'await' expression
3599 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3600 |       Task {
3601 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3602 |       }
3603 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3628:9: warning: no 'async' operations occur within 'await' expression
3626 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3627 |       Task {
3628 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3629 |       }
3630 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3686:9: warning: no 'async' operations occur within 'await' expression
3684 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3685 |       Task {
3686 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3687 |           itemID: item.id,
3688 |           title: item.title.text,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3717:9: warning: no 'async' operations occur within 'await' expression
3715 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3716 |       Task {
3717 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3718 |           itemID: item.id,
3719 |           title: item.title.text,
[194/206] Compiling BobMacCapture CaptureAgendaRowMeasurer.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:2070:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2068 |         }
2069 |         if let textView = firstResponder as? NSTextView,
2070 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2071 |            field.accessibilityIdentifier() == identifier
2072 |         {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:8177:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8175 |         newName: String
 8176 |     ) {
 8177 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8178 |               let rename = current.rename,
 8179 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11085:23: warning: no 'async' operations occur within 'await' expression
11083 |                 }
11084 | 
11085 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11086 |                     return
11087 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11090:21: warning: no 'async' operations occur within 'await' expression
11088 | 
11089 |                 if pickerNeeded == nil {
11090 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11091 |                         draft: draft,
11092 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11104:27: warning: no 'async' operations occur within 'await' expression
11102 |                     await completionGate.value
11103 |                     try Task.checkCancellation()
11104 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11105 |                         return
11106 |                     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11111:20: warning: no 'async' operations occur within 'await' expression
11109 |                 if let cursorUTF8Offset,
11110 |                    requestCompletion,
11111 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11112 |                        parse: parse,
11113 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11117:37: warning: no 'async' operations occur within 'await' expression
11115 |                    ) == true
11116 |                 {
11117 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11118 |                         parse: parse,
11119 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11346:28: warning: no 'async' operations occur within 'await' expression
11344 |         Task { [weak self, processClient] in
11345 |             do {
11346 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
11347 |                 let processClientIdentity = processClient.identityToken
11348 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2330:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
2330 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2331 |     }
2332 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2329:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2327 |         }
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2330 |             + Text(String(label[range.upperBound...]))
2331 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[195/206] Compiling BobMacCapture CaptureAgendaStore.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:2070:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2068 |         }
2069 |         if let textView = firstResponder as? NSTextView,
2070 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2071 |            field.accessibilityIdentifier() == identifier
2072 |         {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:8177:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8175 |         newName: String
 8176 |     ) {
 8177 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8178 |               let rename = current.rename,
 8179 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11085:23: warning: no 'async' operations occur within 'await' expression
11083 |                 }
11084 | 
11085 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11086 |                     return
11087 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11090:21: warning: no 'async' operations occur within 'await' expression
11088 | 
11089 |                 if pickerNeeded == nil {
11090 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11091 |                         draft: draft,
11092 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11104:27: warning: no 'async' operations occur within 'await' expression
11102 |                     await completionGate.value
11103 |                     try Task.checkCancellation()
11104 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11105 |                         return
11106 |                     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11111:20: warning: no 'async' operations occur within 'await' expression
11109 |                 if let cursorUTF8Offset,
11110 |                    requestCompletion,
11111 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11112 |                        parse: parse,
11113 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11117:37: warning: no 'async' operations occur within 'await' expression
11115 |                    ) == true
11116 |                 {
11117 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11118 |                         parse: parse,
11119 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11346:28: warning: no 'async' operations occur within 'await' expression
11344 |         Task { [weak self, processClient] in
11345 |             do {
11346 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
11347 |                 let processClientIdentity = processClient.identityToken
11348 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2330:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
2330 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2331 |     }
2332 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2329:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2327 |         }
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2330 |             + Text(String(label[range.upperBound...]))
2331 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[196/206] Compiling BobMacCapture CaptureAgendaView.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:2070:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2068 |         }
2069 |         if let textView = firstResponder as? NSTextView,
2070 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2071 |            field.accessibilityIdentifier() == identifier
2072 |         {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:8177:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8175 |         newName: String
 8176 |     ) {
 8177 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8178 |               let rename = current.rename,
 8179 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11085:23: warning: no 'async' operations occur within 'await' expression
11083 |                 }
11084 | 
11085 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11086 |                     return
11087 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11090:21: warning: no 'async' operations occur within 'await' expression
11088 | 
11089 |                 if pickerNeeded == nil {
11090 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11091 |                         draft: draft,
11092 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11104:27: warning: no 'async' operations occur within 'await' expression
11102 |                     await completionGate.value
11103 |                     try Task.checkCancellation()
11104 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11105 |                         return
11106 |                     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11111:20: warning: no 'async' operations occur within 'await' expression
11109 |                 if let cursorUTF8Offset,
11110 |                    requestCompletion,
11111 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11112 |                        parse: parse,
11113 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11117:37: warning: no 'async' operations occur within 'await' expression
11115 |                    ) == true
11116 |                 {
11117 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11118 |                         parse: parse,
11119 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11346:28: warning: no 'async' operations occur within 'await' expression
11344 |         Task { [weak self, processClient] in
11345 |             do {
11346 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
11347 |                 let processClientIdentity = processClient.identityToken
11348 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2330:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
2330 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2331 |     }
2332 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2329:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2327 |         }
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2330 |             + Text(String(label[range.upperBound...]))
2331 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[197/206] Compiling BobMacCapture CaptureEditorPalette.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:2070:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2068 |         }
2069 |         if let textView = firstResponder as? NSTextView,
2070 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2071 |            field.accessibilityIdentifier() == identifier
2072 |         {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:8177:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8175 |         newName: String
 8176 |     ) {
 8177 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8178 |               let rename = current.rename,
 8179 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11085:23: warning: no 'async' operations occur within 'await' expression
11083 |                 }
11084 | 
11085 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11086 |                     return
11087 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11090:21: warning: no 'async' operations occur within 'await' expression
11088 | 
11089 |                 if pickerNeeded == nil {
11090 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11091 |                         draft: draft,
11092 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11104:27: warning: no 'async' operations occur within 'await' expression
11102 |                     await completionGate.value
11103 |                     try Task.checkCancellation()
11104 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11105 |                         return
11106 |                     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11111:20: warning: no 'async' operations occur within 'await' expression
11109 |                 if let cursorUTF8Offset,
11110 |                    requestCompletion,
11111 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11112 |                        parse: parse,
11113 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11117:37: warning: no 'async' operations occur within 'await' expression
11115 |                    ) == true
11116 |                 {
11117 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11118 |                         parse: parse,
11119 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11346:28: warning: no 'async' operations occur within 'await' expression
11344 |         Task { [weak self, processClient] in
11345 |             do {
11346 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
11347 |                 let processClientIdentity = processClient.identityToken
11348 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2330:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
2330 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2331 |     }
2332 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2329:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2327 |         }
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2330 |             + Text(String(label[range.upperBound...]))
2331 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[198/206] Compiling BobMacCapture CaptureEditorTextConfiguration.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:2070:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2068 |         }
2069 |         if let textView = firstResponder as? NSTextView,
2070 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2071 |            field.accessibilityIdentifier() == identifier
2072 |         {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:8177:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8175 |         newName: String
 8176 |     ) {
 8177 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8178 |               let rename = current.rename,
 8179 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11085:23: warning: no 'async' operations occur within 'await' expression
11083 |                 }
11084 | 
11085 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11086 |                     return
11087 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11090:21: warning: no 'async' operations occur within 'await' expression
11088 | 
11089 |                 if pickerNeeded == nil {
11090 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11091 |                         draft: draft,
11092 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11104:27: warning: no 'async' operations occur within 'await' expression
11102 |                     await completionGate.value
11103 |                     try Task.checkCancellation()
11104 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11105 |                         return
11106 |                     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11111:20: warning: no 'async' operations occur within 'await' expression
11109 |                 if let cursorUTF8Offset,
11110 |                    requestCompletion,
11111 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11112 |                        parse: parse,
11113 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11117:37: warning: no 'async' operations occur within 'await' expression
11115 |                    ) == true
11116 |                 {
11117 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11118 |                         parse: parse,
11119 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11346:28: warning: no 'async' operations occur within 'await' expression
11344 |         Task { [weak self, processClient] in
11345 |             do {
11346 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
11347 |                 let processClientIdentity = processClient.identityToken
11348 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2330:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
2330 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2331 |     }
2332 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2329:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2327 |         }
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2330 |             + Text(String(label[range.upperBound...]))
2331 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[199/206] Compiling BobMacCapture CaptureInboxRouteChoiceView.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:2070:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2068 |         }
2069 |         if let textView = firstResponder as? NSTextView,
2070 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2071 |            field.accessibilityIdentifier() == identifier
2072 |         {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:8177:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8175 |         newName: String
 8176 |     ) {
 8177 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8178 |               let rename = current.rename,
 8179 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11085:23: warning: no 'async' operations occur within 'await' expression
11083 |                 }
11084 | 
11085 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11086 |                     return
11087 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11090:21: warning: no 'async' operations occur within 'await' expression
11088 | 
11089 |                 if pickerNeeded == nil {
11090 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11091 |                         draft: draft,
11092 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11104:27: warning: no 'async' operations occur within 'await' expression
11102 |                     await completionGate.value
11103 |                     try Task.checkCancellation()
11104 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11105 |                         return
11106 |                     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11111:20: warning: no 'async' operations occur within 'await' expression
11109 |                 if let cursorUTF8Offset,
11110 |                    requestCompletion,
11111 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11112 |                        parse: parse,
11113 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11117:37: warning: no 'async' operations occur within 'await' expression
11115 |                    ) == true
11116 |                 {
11117 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11118 |                         parse: parse,
11119 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11346:28: warning: no 'async' operations occur within 'await' expression
11344 |         Task { [weak self, processClient] in
11345 |             do {
11346 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
11347 |                 let processClientIdentity = processClient.identityToken
11348 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2330:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
2330 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2331 |     }
2332 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2329:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2327 |         }
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2330 |             + Text(String(label[range.upperBound...]))
2331 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[200/206] Compiling BobMacCapture CaptureKeyCommandRouter.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:2070:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2068 |         }
2069 |         if let textView = firstResponder as? NSTextView,
2070 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2071 |            field.accessibilityIdentifier() == identifier
2072 |         {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:8177:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8175 |         newName: String
 8176 |     ) {
 8177 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8178 |               let rename = current.rename,
 8179 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11085:23: warning: no 'async' operations occur within 'await' expression
11083 |                 }
11084 | 
11085 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11086 |                     return
11087 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11090:21: warning: no 'async' operations occur within 'await' expression
11088 | 
11089 |                 if pickerNeeded == nil {
11090 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11091 |                         draft: draft,
11092 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11104:27: warning: no 'async' operations occur within 'await' expression
11102 |                     await completionGate.value
11103 |                     try Task.checkCancellation()
11104 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11105 |                         return
11106 |                     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11111:20: warning: no 'async' operations occur within 'await' expression
11109 |                 if let cursorUTF8Offset,
11110 |                    requestCompletion,
11111 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11112 |                        parse: parse,
11113 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11117:37: warning: no 'async' operations occur within 'await' expression
11115 |                    ) == true
11116 |                 {
11117 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11118 |                         parse: parse,
11119 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11346:28: warning: no 'async' operations occur within 'await' expression
11344 |         Task { [weak self, processClient] in
11345 |             do {
11346 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
11347 |                 let processClientIdentity = processClient.identityToken
11348 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2330:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
2330 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2331 |     }
2332 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2329:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2327 |         }
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2330 |             + Text(String(label[range.upperBound...]))
2331 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[201/206] Compiling BobMacCapture CapturePanelController.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:2070:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2068 |         }
2069 |         if let textView = firstResponder as? NSTextView,
2070 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2071 |            field.accessibilityIdentifier() == identifier
2072 |         {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:8177:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8175 |         newName: String
 8176 |     ) {
 8177 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8178 |               let rename = current.rename,
 8179 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11085:23: warning: no 'async' operations occur within 'await' expression
11083 |                 }
11084 | 
11085 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11086 |                     return
11087 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11090:21: warning: no 'async' operations occur within 'await' expression
11088 | 
11089 |                 if pickerNeeded == nil {
11090 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11091 |                         draft: draft,
11092 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11104:27: warning: no 'async' operations occur within 'await' expression
11102 |                     await completionGate.value
11103 |                     try Task.checkCancellation()
11104 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11105 |                         return
11106 |                     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11111:20: warning: no 'async' operations occur within 'await' expression
11109 |                 if let cursorUTF8Offset,
11110 |                    requestCompletion,
11111 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11112 |                        parse: parse,
11113 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11117:37: warning: no 'async' operations occur within 'await' expression
11115 |                    ) == true
11116 |                 {
11117 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11118 |                         parse: parse,
11119 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11346:28: warning: no 'async' operations occur within 'await' expression
11344 |         Task { [weak self, processClient] in
11345 |             do {
11346 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
11347 |                 let processClientIdentity = processClient.identityToken
11348 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2330:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
2330 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2331 |     }
2332 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2329:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2327 |         }
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2330 |             + Text(String(label[range.upperBound...]))
2331 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[202/206] Compiling BobMacCapture CapturePanelModel.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:2070:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2068 |         }
2069 |         if let textView = firstResponder as? NSTextView,
2070 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2071 |            field.accessibilityIdentifier() == identifier
2072 |         {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:8177:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8175 |         newName: String
 8176 |     ) {
 8177 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8178 |               let rename = current.rename,
 8179 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11085:23: warning: no 'async' operations occur within 'await' expression
11083 |                 }
11084 | 
11085 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11086 |                     return
11087 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11090:21: warning: no 'async' operations occur within 'await' expression
11088 | 
11089 |                 if pickerNeeded == nil {
11090 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11091 |                         draft: draft,
11092 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11104:27: warning: no 'async' operations occur within 'await' expression
11102 |                     await completionGate.value
11103 |                     try Task.checkCancellation()
11104 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11105 |                         return
11106 |                     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11111:20: warning: no 'async' operations occur within 'await' expression
11109 |                 if let cursorUTF8Offset,
11110 |                    requestCompletion,
11111 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11112 |                        parse: parse,
11113 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11117:37: warning: no 'async' operations occur within 'await' expression
11115 |                    ) == true
11116 |                 {
11117 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11118 |                         parse: parse,
11119 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11346:28: warning: no 'async' operations occur within 'await' expression
11344 |         Task { [weak self, processClient] in
11345 |             do {
11346 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
11347 |                 let processClientIdentity = processClient.identityToken
11348 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2330:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
2330 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2331 |     }
2332 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2329:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2327 |         }
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2330 |             + Text(String(label[range.upperBound...]))
2331 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[203/206] Compiling BobMacCapture CapturePanelView.swift
/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 | 
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelController.swift:2070:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2068 |         }
2069 |         if let textView = firstResponder as? NSTextView,
2070 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2071 |            field.accessibilityIdentifier() == identifier
2072 |         {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:2258:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2256 |                         requireInboxRouteChoice: true,
 2257 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2258 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2259 |                     )
 2260 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:8177:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8175 |         newName: String
 8176 |     ) {
 8177 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8178 |               let rename = current.rename,
 8179 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11085:23: warning: no 'async' operations occur within 'await' expression
11083 |                 }
11084 | 
11085 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11086 |                     return
11087 |                 }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11090:21: warning: no 'async' operations occur within 'await' expression
11088 | 
11089 |                 if pickerNeeded == nil {
11090 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11091 |                         draft: draft,
11092 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11104:27: warning: no 'async' operations occur within 'await' expression
11102 |                     await completionGate.value
11103 |                     try Task.checkCancellation()
11104 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11105 |                         return
11106 |                     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11111:20: warning: no 'async' operations occur within 'await' expression
11109 |                 if let cursorUTF8Offset,
11110 |                    requestCompletion,
11111 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11112 |                        parse: parse,
11113 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11117:37: warning: no 'async' operations occur within 'await' expression
11115 |                    ) == true
11116 |                 {
11117 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11118 |                         parse: parse,
11119 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelModel.swift:11346:28: warning: no 'async' operations occur within 'await' expression
11344 |         Task { [weak self, processClient] in
11345 |             do {
11346 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
11347 |                 let processClientIdentity = processClient.identityToken
11348 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2330:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
2330 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2331 |     }
2332 | 

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/CapturePanelView.swift:2329:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2327 |         }
2328 |         return Text(String(label[..<range.lowerBound]))
2329 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2330 |             + Text(String(label[range.upperBound...]))
2331 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[203/206] Write Objects.LinkFileList
[204/206] Linking BobMacCapture
[205/206] Applying BobMacCapture
Build complete! (89.36s)
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

Tests/BobMacCaptureTests/CaptureAgendaStoreTests.swift:340:13: warning: initialization of immutable value 'store' was never used; consider replacing with assignment to '_' or removing it [#no-usage]
338 |         let workspaceCenter = NotificationCenter()
339 |         let defaultCenter = NotificationCenter()
340 |         let store = try makeStore(
    |             `- warning: initialization of immutable value 'store' was never used; consider replacing with assignment to '_' or removing it [#no-usage]
341 |             recordURL: recordURL,
342 |             workspaceCenter: workspaceCenter,

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:240:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
238 |         XCTAssertNil(model.completionResponse)
239 |         XCTAssertNil(model.picker)
240 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
241 |         XCTAssertTrue(record.contains("argv=capture-rewrite --cursor 17 --format json -- Do work @file:id^"))
242 |         XCTAssertFalse(record.contains("capture-complete --all-tasks --cursor 17"))

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:334:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
332 |         XCTAssertEqual(textView.string, "Do work @file:id")
333 | 
334 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
335 |         let rewriteCount = record.components(separatedBy: "argv=capture-rewrite").count - 1
336 |         XCTAssertEqual(rewriteCount, 1)

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:355:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
353 | 
354 |         XCTAssertEqual(model.plainDraft, "Do work @file^id ")
355 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
356 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-rewrite").count - 1, 1)
357 |     }

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:459:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
457 |         XCTAssertEqual(model.statusText, "Pick a task or type a new ID — press Tab to browse")
458 |         XCTAssertEqual(model.plainDraft, "@file:")
459 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
460 |         XCTAssertTrue(record.contains("argv=capture-rewrite --cursor 6 --format json -- @file:"))
461 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 6 --format json -- @file:"))

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:489:27: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
487 |         try await Task.sleep(nanoseconds: 100_000_000)
488 |         XCTAssertFalse(model.pickerVisible)
489 |         let early = (try? String(contentsOf: recordURL)) ?? ""
    |                           `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
490 |         XCTAssertFalse(early.contains("argv=capture-complete"))
491 | 

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:512:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
510 |         XCTAssertEqual(model.plainDraft, "Do work @file^id")
511 |         XCTAssertNil(model.picker)
512 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
513 |         XCTAssertFalse(record.contains("capture-complete --all-tasks --cursor 17"))
514 |     }

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:578:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
576 |         XCTAssertEqual(model.relationLabelPrompt?.targetText, "Target")
577 |         XCTAssertEqual(model.relationLabelPrompt?.labelRange, CaptureRange(start: 22, end: 23))
578 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
579 |         XCTAssertTrue(record.contains("argv=capture-rewrite --cursor 24 --format json -- New task ~tasks:target |"))
580 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 23 --format json -- New task ~tasks:target|"))

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:611:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
609 |         XCTAssertEqual(model.plainDraft, "New task ~tasks:target|")
610 |         XCTAssertEqual(textView.string, "New task ~tasks:target|")
611 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
612 |         XCTAssertTrue(record.contains("argv=capture-rewrite --cursor 23 --format json -- New task ~tasks:target|"))
613 |         XCTAssertTrue(record.contains("capture-complete --all-tasks --cursor 23"))

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:661:19: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
659 |         // Mid-draft caret must request completion at the pipe (23), not end of draft (29).
660 |         await waitUntil {
661 |             (try? String(contentsOf: recordURL))?.contains(
    |                   `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
662 |                 "argv=capture-complete --all-tasks --cursor 23 --format json -- New task ~tasks:target| @work"
663 |             ) == true

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:665:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
663 |             ) == true
664 |         }
665 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
666 |         XCTAssertFalse(record.contains("capture-complete --all-tasks --cursor 29"))
667 |         model.updateRelationLabelPromptLabel("follow")

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:709:19: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
707 |         XCTAssertEqual(model.relationLabelPrompt?.ownerText, "Fix it")
708 |         await waitUntil {
709 |             (try? String(contentsOf: recordURL))?.contains(
    |                   `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
710 |                 "argv=capture-complete --all-tasks --cursor 14 --format json -- ~tasks:target| Fix it"
711 |             ) == true

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:713:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
711 |             ) == true
712 |         }
713 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
714 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 14 --format json -- ~tasks:target| Fix it"))
715 |         model.updateRelationLabelPromptLabel("see")

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:740:19: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
738 |         XCTAssertEqual(model.relationLabelPrompt?.ownerText, "Fix it")
739 |         await waitUntil {
740 |             (try? String(contentsOf: recordURL))?.contains(
    |                   `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
741 |                 "argv=capture-complete --all-tasks --cursor 21 --format json -- Fix it ~tasks:target| &tasks:source"
742 |             ) == true

Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:806:19: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
804 |         XCTAssertEqual(model.relationLabelPrompt?.ownerText, "Hi 🧪")
805 |         await waitUntil {
806 |             (try? String(contentsOf: recordURL))?.contains(
    |                   `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
807 |                 "argv=capture-complete --all-tasks --cursor 22 --format json -- Hi 🧪 ~tasks:target|"
808 |             ) == true

Tests/BobMacCaptureTests/CaptureRelatedLaneTests.swift:64:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 62 |     XCTAssertEqual(model.similarTasks.items.first?.overflowCount, 2)
 63 |     XCTAssertEqual(model.similarTasks.draft, "Install new UPS battery")
 64 |     let record = try String(contentsOf: recordURL)
    |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 65 |     XCTAssertTrue(record.contains("argv=capture-related --format json -- Install new UPS battery"))
 66 |   }

Tests/BobMacCaptureTests/CaptureRelatedLaneTests.swift:87:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 85 |     try await Task.sleep(nanoseconds: 160_000_000)
 86 | 
 87 |     var record = try String(contentsOf: recordURL)
    |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 88 |     XCTAssertEqual(record.components(separatedBy: "argv=capture-related").count - 1, 1)
 89 | 

Tests/BobMacCaptureTests/CaptureRelatedLaneTests.swift:93:18: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 91 |     typeDraft(model, "Buy another UPS battery")
 92 |     try await Task.sleep(nanoseconds: 180_000_000)
 93 |     record = try String(contentsOf: recordURL)
    |                  `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 94 |     XCTAssertEqual(record.components(separatedBy: "argv=capture-related").count - 1, 1)
 95 |     XCTAssertTrue(model.similarTasks.rows.isEmpty)

Tests/BobMacCaptureTests/CaptureRelatedLaneTests.swift:119:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
117 |     XCTAssertTrue(model.similarTasks.rows.isEmpty)
118 |     XCTAssertNil(model.errorMessage)
119 |     let record = try String(contentsOf: recordURL)
    |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
120 |     XCTAssertEqual(record.components(separatedBy: "argv=capture-related").count - 1, 1)
121 |   }

Tests/BobMacCaptureTests/CaptureRelatedLaneTests.swift:148:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
146 |       }
147 |       try await Task.sleep(nanoseconds: 200_000_000)
148 |       let record = (try? String(contentsOf: recordURL)) ?? ""
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
149 |       return record
150 |         .components(separatedBy: "\n")

Tests/BobMacCaptureTests/CaptureRelatedLaneTests.swift:201:30: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
199 |     typeDraft(model, "Install new UPS battery edited")
200 |     try await Task.sleep(nanoseconds: 300_000_000)
201 |     let hiddenRecord = (try? String(contentsOf: recordURL)) ?? ""
    |                              `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
202 |     XCTAssertEqual(hiddenRecord.components(separatedBy: "argv=capture-related").count - 1, 0)
203 |     model.prepareForPresentation()

Tests/BobMacCaptureTests/CaptureRelatedLaneTests.swift:205:29: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
203 |     model.prepareForPresentation()
204 |     await waitUntil { !model.similarTasks.pending && !model.similarTasks.rows.isEmpty }
205 |     let shownRecord = (try? String(contentsOf: recordURL)) ?? ""
    |                             `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
206 |     XCTAssertEqual(shownRecord.components(separatedBy: "argv=capture-related").count - 1, 1)
207 |     XCTAssertEqual(model.similarTasks.draft, "Install new UPS battery edited")

Tests/BobMacCaptureTests/CaptureRelatedLaneTests.swift:224:24: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
222 |     typeDraft(model, "Install new UPS battery")
223 |     await waitUntil { !model.similarTasks.pending && !model.similarTasks.rows.isEmpty }
224 |     let before = (try? String(contentsOf: recordURL)) ?? ""
    |                        `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
225 |     XCTAssertEqual(before.components(separatedBy: "argv=capture-related").count - 1, 1)
226 |     let heldIDs = model.similarTasks.rows.map(\.id)

Tests/BobMacCaptureTests/CaptureRelatedLaneTests.swift:232:23: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
230 |     typeDraft(model, "Install new UPS battery plus cable")
231 |     try await Task.sleep(nanoseconds: 250_000_000)
232 |     let after = (try? String(contentsOf: recordURL)) ?? ""
    |                       `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
233 |     XCTAssertEqual(after.components(separatedBy: "argv=capture-related").count - 1, 1)
234 |     XCTAssertEqual(model.similarTasks.rows.map(\.id), heldIDs)

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

Tests/BobMacCaptureTests/RefsPanelModelTests.swift:2571:24: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2569 |     await harness.waitForModel { _ in harness.library.snapshotRefreshGeneration > generation }
2570 |     try? await Task.sleep(nanoseconds: 100_000_000)
2571 |     let record = (try? String(contentsOf: recordURL)) ?? ""
     |                        `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2572 |     XCTAssertFalse(record.contains("argv=ref show"))
2573 |   }

Tests/BobMacCaptureTests/RefsPanelModelTests.swift:3377:32: error: contextual type for closure argument list expects 1 argument, which cannot be implicitly ignored
3375 |       inspector: [target.id: RefsInspectorContent(highlights: Self.thirteenNotes())]
3376 |     )
3377 |     await harness.waitForModel { !received.isEmpty }
     |                                `- error: contextual type for closure argument list expects 1 argument, which cannot be implicitly ignored
3378 |     let focus = try XCTUnwrap(harness.model.inspectorFocus)
3379 |     XCTAssertEqual(focus.id, target.id)

Tests/BobMacCaptureTests/RefsPanelModelTests.swift:3513:32: error: contextual type for closure argument list expects 1 argument, which cannot be implicitly ignored
3511 |       inspector: [target.id: RefsInspectorContent(highlights: Self.thirteenNotes())]
3512 |     )
3513 |     await harness.waitForModel { received.count == 1 }
     |                                `- error: contextual type for closure argument list expects 1 argument, which cannot be implicitly ignored
3514 |     XCTAssertEqual(harness.model.inspectorFocus?.id, target.id)
3515 |     XCTAssertEqual(received.count, 1)

Tests/BobMacCaptureTests/RefsPanelModelTests.swift:5224:24: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5222 |     await harness.waitForModel { _ in argvCount(recordURL, prefix: "argv=vault-sync -q") == 1 }
5223 |     await harness.waitForModel { _ in argvCount(recordURL, prefix: "argv=ref list") >= 1 }
5224 |     let record = (try? String(contentsOf: recordURL)) ?? ""
     |                        `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5225 |     guard let pullRange = record.range(of: "argv=vault-sync -q"),
5226 |       let listRange = record.range(of: "argv=ref list")

Tests/BobMacCaptureTests/RefsPanelModelTests.swift:6174:24: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6172 | 
6173 |   private func showCount(_ recordURL: URL, path: String) -> Int {
6174 |     let record = (try? String(contentsOf: recordURL)) ?? ""
     |                        `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6175 |     return record.components(separatedBy: "argv=ref show \(path) -f json").count - 1
6176 |   }

Tests/BobMacCaptureTests/RefsPanelModelTests.swift:6327:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6325 | /// How many fake-bob invocations start with `prefix` in a record file.
6326 | private func argvCount(_ recordURL: URL, prefix: String) -> Int {
6327 |   let record = (try? String(contentsOf: recordURL)) ?? ""
     |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6328 |   return record.components(separatedBy: prefix).count - 1
6329 | }

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

Tests/BobMacCaptureTests/CaptureSavedTemplateShelfTests.swift:177:31: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
175 | 
176 |     private func recordArgvCount(_ url: URL) -> Int {
177 |         guard let text = try? String(contentsOf: url) else {
    |                               `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
178 |             return 0
179 |         }

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

Tests/BobMacCaptureTests/RefsInspectorTests.swift:838:16: warning: no 'async' operations occur within 'await' expression
 836 |     let root = FileManager.default.temporaryDirectory
 837 |       .appendingPathComponent(UUID().uuidString)
 838 |     let slow = await RefsPDFIntrinsicsLoader(
     |                `- warning: no 'async' operations occur within 'await' expression
 839 |       cacheDirectory: root,
 840 |       reader: { @Sendable _ in

Tests/BobMacCaptureTests/RefsInspectorTests.swift:856:16: warning: no 'async' operations occur within 'await' expression
 854 |     // The abandoned read never queues later loads behind it: a
 855 |     // fresh loader answers at once.
 856 |     let fast = await RefsPDFIntrinsicsLoader(
     |                `- warning: no 'async' operations occur within 'await' expression
 857 |       cacheDirectory: root,
 858 |       reader: { @Sendable _ in RefsPDFIntrinsics(pageCount: 3) }

Tests/BobMacCaptureTests/RefsInspectorTests.swift:869:18: warning: no 'async' operations occur within 'await' expression
 867 |     let root = FileManager.default.temporaryDirectory
 868 |       .appendingPathComponent(UUID().uuidString)
 869 |     let loader = await RefsPDFIntrinsicsLoader(
     |                  `- warning: no 'async' operations occur within 'await' expression
 870 |       cacheDirectory: root,
 871 |       reader: { @Sendable _ in

Tests/BobMacCaptureTests/RefsInspectorTests.swift:936:18: warning: no 'async' operations occur within 'await' expression
 934 |       contents: Data("{}".utf8)
 935 |     )
 936 |     let loader = await RefsPDFIntrinsicsLoader(
     |                  `- warning: no 'async' operations occur within 'await' expression
 937 |       cacheDirectory: root,
 938 |       reader: { @Sendable _ in

Tests/BobMacCaptureTests/RefsInspectorTests.swift:1021:18: warning: no 'async' operations occur within 'await' expression
1019 |     let root = FileManager.default.temporaryDirectory
1020 |       .appendingPathComponent(UUID().uuidString)
1021 |     let loader = await RefsPDFIntrinsicsLoader(
     |                  `- warning: no 'async' operations occur within 'await' expression
1022 |       cacheDirectory: root,
1023 |       reader: { @Sendable _ in

Tests/BobMacCaptureTests/CaptureShowRefreshWindowTests.swift:40:25: warning: main actor-isolated class property 'pullThrottleInterval' can not be referenced from a nonisolated autoclosure; this is an error in the Swift 6 language mode
38 |         XCTAssertEqual(
39 |             CaptureShowRefreshWindow.pullThrottleInterval,
40 |             RefsLibrary.pullThrottleInterval
   |                         `- warning: main actor-isolated class property 'pullThrottleInterval' can not be referenced from a nonisolated autoclosure; this is an error in the Swift 6 language mode
41 |         )
42 |     }

/private/tmp/bob-mac-capture-check.3Q9EC7/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:21: note: class property declared here
 170 | 
 171 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: class property declared here
 173 | 
 174 |   private var fetcher: RefsFetching?

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

Tests/BobMacCaptureTests/CaptureTargetsRefreshGateTests.swift:15:53: warning: reference to captured var 'current' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
13 |     func testShowInsideWindowSkips() {
14 |         var current = Date(timeIntervalSince1970: 1_000)
15 |         var gate = CaptureTargetsRefreshGate(now: { current })
   |                                                     `- warning: reference to captured var 'current' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
16 |         XCTAssertTrue(gate.shouldRefresh(reason: .show))
17 |         current = Date(timeIntervalSince1970: 1_003)

Tests/BobMacCaptureTests/CaptureTargetsRefreshGateTests.swift:25:53: warning: reference to captured var 'current' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
23 |     func testShowAtBoundaryRuns() {
24 |         var current = Date(timeIntervalSince1970: 1_000)
25 |         var gate = CaptureTargetsRefreshGate(now: { current })
   |                                                     `- warning: reference to captured var 'current' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
26 |         XCTAssertTrue(gate.shouldRefresh(reason: .show))
27 |         current = Date(timeIntervalSince1970: 1_000)

Tests/BobMacCaptureTests/CaptureTargetsRefreshGateTests.swift:35:53: warning: reference to captured var 'current' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
33 |     func testShowOutsideWindowRuns() {
34 |         var current = Date(timeIntervalSince1970: 1_000)
35 |         var gate = CaptureTargetsRefreshGate(now: { current })
   |                                                     `- warning: reference to captured var 'current' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
36 |         XCTAssertTrue(gate.shouldRefresh(reason: .show))
37 |         current = Date(timeIntervalSince1970: 1_000)

Tests/BobMacCaptureTests/CaptureTargetsRefreshGateTests.swift:44:53: warning: reference to captured var 'current' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
42 |     func testNonShowReasonsBypassInsideWindow() {
43 |         var current = Date(timeIntervalSince1970: 1_000)
44 |         var gate = CaptureTargetsRefreshGate(now: { current })
   |                                                     `- warning: reference to captured var 'current' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
45 |         XCTAssertTrue(gate.shouldRefresh(reason: .show))
46 |         current = Date(timeIntervalSince1970: 1_001)

Tests/BobMacCaptureTests/CaptureTargetsRefreshGateTests.swift:57:13: warning: mutation of captured var 'calls' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
55 |         var current = Date(timeIntervalSince1970: 2_000)
56 |         var gate = CaptureTargetsRefreshGate(now: {
57 |             calls += 1
   |             `- warning: mutation of captured var 'calls' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
58 |             return current
59 |         })

Tests/BobMacCaptureTests/CaptureTargetsRefreshGateTests.swift:58:20: warning: reference to captured var 'current' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
56 |         var gate = CaptureTargetsRefreshGate(now: {
57 |             calls += 1
58 |             return current
   |                    `- warning: reference to captured var 'current' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
59 |         })
60 |         XCTAssertTrue(gate.shouldRefresh(reason: .show))

Tests/BobMacCaptureTests/RefsEntryPointsTests.swift:1069:24: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1067 | 
1068 |   private func entryPointsPlanCount(_ recordURL: URL) -> Int {
1069 |     let record = (try? String(contentsOf: recordURL)) ?? ""
     |                        `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1070 |     return record.components(separatedBy: "argv=plan -f json").count - 1
1071 |   }

Tests/BobMacCaptureTests/SimilarTasksActionsTests.swift:246:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
244 |     await waitUntil { !model.similarTasks.pending && !model.similarTasks.rows.isEmpty }
245 |     try await Task.sleep(nanoseconds: 160_000_000)
246 |     var record = try String(contentsOf: recordURL)
    |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
247 |     let settledCount = record.components(separatedBy: "argv=capture-related").count - 1
248 | 

Tests/BobMacCaptureTests/SimilarTasksActionsTests.swift:256:18: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
254 |     await waitUntil { !model.similarTasks.pending || model.similarTasks.focusedRowID != nil }
255 |     try await Task.sleep(nanoseconds: 200_000_000)
256 |     record = try String(contentsOf: recordURL)
    |                  `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
257 |     let total = record.components(separatedBy: "argv=capture-related").count - 1
258 |     XCTAssertGreaterThanOrEqual(total, settledCount + 1)

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

Tests/BobMacCaptureTests/RefsLibraryTests.swift:283:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 281 |     try? await Task.sleep(nanoseconds: 3_000_000_000)
 282 | 
 283 |     let record = try String(contentsOf: recordURL)
     |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 284 |     XCTAssertEqual(record.components(separatedBy: "argv=ref list").count - 1, 2)
 285 |   }

Tests/BobMacCaptureTests/RefsLibraryTests.swift:404:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 402 |     context.library.refreshToday(reason: .manual)
 403 |     await waitUntil(timeout: 15) {
 404 |       let record = (try? String(contentsOf: recordURL)) ?? ""
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 405 |       return record.components(separatedBy: "argv=plan -f json").count == 3
 406 |     }

Tests/BobMacCaptureTests/RefsLibraryTests.swift:479:27: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 477 |       }
 478 |     }
 479 |     let staleRecord = try String(contentsOf: recordURL)
     |                           `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 480 |     let count = staleRecord.components(separatedBy: "argv=").count
 481 | 

Tests/BobMacCaptureTests/RefsLibraryTests.swift:484:27: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 482 |     context.library.refreshIfStale()
 483 |     try? await Task.sleep(nanoseconds: 1_000_000_000)
 484 |     let quietRecord = try String(contentsOf: recordURL)
     |                           `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 485 |     XCTAssertEqual(quietRecord.components(separatedBy: "argv=").count, count)
 486 | 

Tests/BobMacCaptureTests/RefsLibraryTests.swift:490:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 488 |     context.library.refreshIfStale()
 489 |     await waitUntil(timeout: 15) {
 490 |       let record = (try? String(contentsOf: recordURL)) ?? ""
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 491 |       return record.components(separatedBy: "argv=").count > count
 492 |     }

Tests/BobMacCaptureTests/RefsLibraryTests.swift:542:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 540 |       return false
 541 |     }
 542 |     let record = try String(contentsOf: recordURL)
     |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 543 |     XCTAssertEqual(
 544 |       record.components(separatedBy: "argv=ref scan -a -w -f json").count - 1,

Tests/BobMacCaptureTests/RefsLibraryTests.swift:572:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 570 |       return false
 571 |     }
 572 |     let record = try String(contentsOf: recordURL)
     |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 573 |     XCTAssertEqual(
 574 |       record.components(separatedBy: "argv=ref scan -a -w -f json").count - 1,

Tests/BobMacCaptureTests/RefsLibraryTests.swift:603:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 601 |     XCTAssertEqual(context.library.requestScan(queueIfBusy: true), .queued)
 602 |     await waitUntil(timeout: 15) {
 603 |       let record = (try? String(contentsOf: recordURL)) ?? ""
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 604 |       return record.components(separatedBy: "argv=ref scan -a -w -f json").count - 1 == 2
 605 |         && transitions.filter { $0 == "finished" }.count == 2

Tests/BobMacCaptureTests/RefsLibraryTests.swift:629:14: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 627 |     }
 628 |     await waitUntil(timeout: 5) {
 629 |       ((try? String(contentsOf: recordURL)) ?? "")
     |              `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 630 |         .contains("argv=ref rename -f json")
 631 |     }

Tests/BobMacCaptureTests/RefsLibraryTests.swift:636:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 634 |     _ = try await rename.value
 635 |     await waitUntil(timeout: 15) {
 636 |       let record = (try? String(contentsOf: recordURL)) ?? ""
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 637 |       let finished: Bool
 638 |       if case .finished = context.library.scanState {

Tests/BobMacCaptureTests/RefsLibraryTests.swift:646:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 644 |         && finished
 645 |     }
 646 |     let record = try String(contentsOf: recordURL)
     |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 647 |     guard let renameRange = record.range(of: "argv=ref rename -f json"),
 648 |       let scanRange = record.range(of: "argv=ref scan -a -w -f json")

Tests/BobMacCaptureTests/RefsLibraryTests.swift:687:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 685 |         $0.id == "ref/papers/harness_notes.md"
 686 |       })
 687 |     let record = try String(contentsOf: recordURL)
     |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 688 |     guard let scanRange = record.range(of: "argv=ref scan -a -w -f json"),
 689 |       let listRange = record.range(of: "argv=ref list -R all -A -f json")

Tests/BobMacCaptureTests/RefsLibraryTests.swift:711:27: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 709 |     context.library.handleWatcherChange()
 710 |     try? await Task.sleep(nanoseconds: 500_000_000)
 711 |     let midRecord = (try? String(contentsOf: recordURL)) ?? ""
     |                           `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 712 |     XCTAssertFalse(midRecord.contains("argv=ref list"))
 713 |     await waitUntil(timeout: 15) {

Tests/BobMacCaptureTests/RefsLibraryTests.swift:720:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 718 |     }
 719 |     try? await Task.sleep(nanoseconds: 500_000_000)
 720 |     let record = try String(contentsOf: recordURL)
     |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 721 |     XCTAssertEqual(
 722 |       record.components(separatedBy: "argv=ref list -R all -A -f json").count - 1,

Tests/BobMacCaptureTests/RefsLibraryTests.swift:1122:14: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1120 |     await context.library.pullAndWait()
1121 |     await waitUntil(timeout: 5) {
1122 |       ((try? String(contentsOf: recordURL)) ?? "").contains("argv=vault-sync -q")
     |              `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1123 |     }
1124 |     guard case .idle = context.library.refreshState else {

Tests/BobMacCaptureTests/RefsLibraryTests.swift:1271:9: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1269 | 
1270 |   private func planCallCount(_ recordURL: URL) throws -> Int {
1271 |     try String(contentsOf: recordURL)
     |         `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1272 |       .components(separatedBy: "argv=plan -f json").count - 1
1273 |   }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:654:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 652 |         XCTAssertEqual(model.lastSuccess?.toggleBehavior, "ensure_next")
 653 |         XCTAssertEqual(model.lastSuccess?.pomodoroLinkAction, "moved")
 654 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 655 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- @file+goog-exit"))
 656 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- @file+goog-exit"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:693:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 691 |         XCTAssertNil(model.lastSuccess?.toggleBehavior)
 692 |         XCTAssertEqual(model.lastSuccess?.toggleDirection, "next")
 693 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 694 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- @file+goog-exit!"))
 695 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- @file+goog-exit!"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:770:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 768 |         XCTAssertTrue(model.previewResults.isEmpty)
 769 |         XCTAssertEqual(model.statusText, "Pick an active task — press Tab to browse")
 770 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 771 |         XCTAssertFalse(record.contains("argv=capture --dry-run"))
 772 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 1)

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:800:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 798 |         XCTAssertEqual(model.statusText, "Pick any open task — press Tab to browse")
 799 |         XCTAssertEqual(model.previewState, .idle)
 800 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 801 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 1)
 802 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:829:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 827 |         XCTAssertEqual(model.picker?.source, .taskLink)
 828 |         XCTAssertEqual(model.picker?.candidates.count, 8)
 829 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 830 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 1)
 831 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:860:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 858 |         XCTAssertEqual(model.picker?.candidates.count, 8)
 859 |         XCTAssertNil(model.completionResponse)
 860 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 861 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 11 --format json -- "))
 862 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:882:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 880 |         await waitUntil { model.pickerVisible }
 881 | 
 882 |         let before = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 883 |         XCTAssertEqual(before.components(separatedBy: "argv=capture-complete").count - 1, 1)
 884 | 

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:891:25: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 889 |         XCTAssertEqual(model.picker?.filterText, "deep")
 890 |         XCTAssertEqual(model.pickerPresentation?.mode, .filtered)
 891 |         let after = try String(contentsOf: recordURL)
     |                         `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 892 |         XCTAssertEqual(after.components(separatedBy: "argv=capture-complete").count - 1, 1)
 893 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:902:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 900 | 
 901 |         XCTAssertEqual(model.picker?.source, .taskLink)
 902 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 903 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 1)
 904 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:923:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 921 |         XCTAssertEqual(model.picker?.snapshotIsPartial, true)
 922 |         XCTAssertEqual(model.pickerPresentation?.mode, .filtered)
 923 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 924 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 2)
 925 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 0 "))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:967:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 965 |         XCTAssertFalse(model.pickerVisible)
 966 |         XCTAssertEqual(model.lastSuccess?.kind, "pomodoro_link")
 967 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
 968 |         XCTAssertTrue(record.contains("argv=capture --format json --refuse-override -- @sase:deep-fix"))
 969 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1050:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1048 | 
1049 |         XCTAssertEqual(model.collapsedSelectionUTF8Offset(), 21)
1050 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1051 |         XCTAssertTrue(
1052 |             record.contains(

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1082:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1080 | 
1081 |         XCTAssertEqual(model.lastSuccess?.kind, "pomodoro_link")
1082 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1083 |         XCTAssertTrue(record.contains("argv=capture --format json --refuse-override -- @sase:fix-flaky-gkeep"))
1084 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1107:17: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1105 |         XCTAssertEqual(openedURL?.host, "bob-open-notes")
1106 |         XCTAssertTrue(
1107 |             try String(contentsOf: recordURL).contains(
     |                 `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1108 |                 "argv=capture --format json --refuse-override -- @sase:fix-flaky-gkeep"
1109 |             )

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1153:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1151 |         XCTAssertEqual(model.picker?.snapshotIsPartial, false)
1152 |         XCTAssertEqual(model.pickerPresentation?.mode, .filtered)
1153 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1154 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 2)
1155 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 1 "))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1255:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1253 |         XCTAssertFalse(model.pickerChipVisible)
1254 |         XCTAssertNil(model.completionResponse)
1255 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1256 |         XCTAssertTrue(
1257 |             record.contains("argv=capture --dry-run --no-clip --format json -- ^sase:deep-fix")

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1517:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1515 |         XCTAssertEqual(model.statusText, "Pick a task or type a new ID — press Tab to browse")
1516 |         XCTAssertEqual(model.previewState, .idle)
1517 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1518 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- @file:"))
1519 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 6 --format json -- @file:"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1544:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1542 |         XCTAssertEqual(model.picker?.snapshotIsPartial, false)
1543 |         XCTAssertEqual(model.pickerPresentation?.mode, .filtered)
1544 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1545 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 6 --format json -- @file:rea"))
1546 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1818:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1816 |         XCTAssertFalse(model.pickerVisible)
1817 |         XCTAssertTrue(model.completionVisible)
1818 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
1819 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 23 --format json -- Follow up @file:new-id#"))
1820 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2320:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2318 |             "Closed CAPTURE · 1 started · 3 Work Log entries"
2319 |         )
2320 |         let record = try String(cFAIL BobMacCaptureTests
ontentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2321 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- \(draft)"))
2322 |         XCTAssertTrue(record.contains("argv=capture --format json --refuse-override -- \(draft)"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2483:30: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2481 |             model.submit(openAfterCapture: false)
2482 |             await waitUntil { !model.isSubmitting }
2483 |             let record = try String(contentsOf: recordURL)
     |                              `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2484 |             let invocations = record.split(separator: "\n")
2485 |                 .filter { $0.hasPrefix("argv=capture --") && !$0.contains("--dry-run") }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2535:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2533 |         model.submit(openAfterCapture: false)
2534 |         XCTAssertFalse(model.isSubmitting)
2535 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2536 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- x*1\n"))
2537 |         XCTAssertFalse(record.contains("argv=capture --format json --refuse-override -- x*1,"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2975:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2973 |         XCTAssertFalse(model.isSubmitting)
2974 |         XCTAssertEqual(model.statusText, "Type a task number after ~ — Start is disabled")
2975 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
2976 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- =\n"))
2977 |         XCTAssertFalse(record.contains("argv=capture --format json --refuse-override -- =~"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3024:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3022 |         XCTAssertFalse(model.isSubmitting)
3023 |         XCTAssertEqual(model.statusText, "Type a task number after , — Close is disabled")
3024 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3025 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- x1\n"))
3026 |         XCTAssertFalse(record.contains("argv=capture --format json --refuse-override -- x1,"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3071:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3069 |         model.submit(openAfterCapture: false)
3070 |         XCTAssertFalse(model.isSubmitting)
3071 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3072 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- x\n"))
3073 |         XCTAssertFalse(record.contains("argv=capture --format json --refuse-override -- x\n- 1"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3119:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3117 |             ["sketched the URL parser"]
3118 |         )
3119 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3120 |         XCTAssertTrue(
3121 |             record.contains(

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3197:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3195 |             "Started CAPTURE 0945-1010 (25m) at line 4"
3196 |         )
3197 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3198 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- \(draft)"))
3199 |         XCTAssertTrue(record.contains("argv=capture --format json --refuse-override -- \(draft)"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3277:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3275 |             "Restarted CAPTURE 0920-0945 → 0935-1000 (25m) at line 5"
3276 |         )
3277 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3278 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- \(draft)"))
3279 |         let invocations = record.split(separator: "\n")

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3308:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3306 |         await waitUntil { !model.isSubmitting }
3307 | 
3308 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3309 |         XCTAssertTrue(record.contains("argv=capture --format json --refuse-override -- ="))
3310 |         XCTAssertFalse(record.contains("argv=capture --dry-run"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3334:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3332 |         XCTAssertEqual(model.plainDraft, "")
3333 |         XCTAssertTrue(model.processClient?.refuseOverrideKnownUnsupported == true)
3334 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3335 |         let invocations = record.split(separator: "\n").filter { $0.hasPrefix("argv=capture --") }
3336 |         XCTAssertEqual(invocations.count, 2, record)

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3426:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3424 |         await waitUntil { !model.isSubmitting }
3425 | 
3426 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3427 |         XCTAssertTrue(
3428 |             record.contains("argv=capture --format json --refuse-override -- \(stale)")

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3525:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3523 |         XCTAssertEqual(model.completionResponse?.candidates.count, 4)
3524 |         XCTAssertEqual(model.completionResponse?.candidates.first?.replacement, "bugs")
3525 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3526 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 2 --format json -- =#"))
3527 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3576:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3574 |             CaptureRange(start: 4, end: 6)
3575 |         )
3576 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3577 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 6 --format json -- x =#de"))
3578 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3602:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3600 |         XCTAssertNil(model.completionResponse)
3601 |         XCTAssertFalse(model.completionVisible)
3602 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3603 |         XCTAssertFalse(record.contains("argv=capture-complete"))
3604 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3629:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3627 |         XCTAssertEqual(model.statusText, "Pick a Pomodoro to start, or type a new name")
3628 |         XCTAssertTrue(model.completionVisible)
3629 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3630 |         XCTAssertFalse(record.contains("argv=capture --dry-run"))
3631 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3918:30: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3916 |         XCTAssertNotNil(model.closePresentation)
3917 |         let dryRunLine = "argv=capture --dry-run --no-clip --format json -- x"
3918 |         let runsBefore = try String(contentsOf: recordURL)
     |                              `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3919 |             .components(separatedBy: dryRunLine).count - 1
3920 |         XCTAssertEqual(runsBefore, 1)

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3929:30: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3927 |                 return false
3928 |             }
3929 |             let runs = (try? String(contentsOf: recordURL))?
     |                              `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
3930 |                 .components(separatedBy: dryRunLine).count ?? 1
3931 |             return runs - 1 == 2

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4097:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4095 | 
4096 |         XCTAssertEqual(model.lastSuccess?.pomodoroStart?.durationMinutes, 15)
4097 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4098 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- \(draft)"))
4099 |         XCTAssertTrue(record.contains("argv=capture --format json --refuse-override -- \(draft)"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4160:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4158 |         XCTAssertEqual(model.lastSuccess?.pomodoroAdjust?.deltaMinutes, 25)
4159 |         XCTAssertFalse(model.lastSuccess?.dryRun ?? true)
4160 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4161 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- \(draft)"))
4162 |         XCTAssertTrue(record.contains("argv=capture --format json --refuse-override -- \(draft)"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4453:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4451 |         XCTAssertEqual(model.lastSuccess?.toggleBehavior, "ensure_next")
4452 |         XCTAssertEqual(model.lastSuccess?.pomodoroLinkAction, "moved")
4453 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4454 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- @file+goog-exit#coding"))
4455 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- @file+goog-exit#coding"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4754:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4752 |         }
4753 | 
4754 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4755 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- Restored café @Cash\n- child"))
4756 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- Restored café @Cash\n- child"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4843:28: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4841 |         await waitUntil { !model.isSubmitting }
4842 | 
4843 |         let record = (try? String(contentsOf: recordURL)) ?? ""
     |                            `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4844 |         let invocationCount = record.components(separatedBy: "argv=")
4845 |             .dropFirst()

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4869:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4867 |         XCTAssertEqual(model.plainDraft, "Call bank @Cash")
4868 |         XCTAssertTrue(model.previewResult?.dryRun ?? false)
4869 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4870 |         XCTAssertTrue(record.contains("--dry-run"))
4871 |         XCTAssertFalse(record.contains("--no-clip"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4905:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4903 | 
4904 |         XCTAssertEqual(model.collapsedSelectionUTF8Offset(), "Buy milk @@dev".utf8.count)
4905 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4906 |         XCTAssertTrue(record.contains("argv=capture-rewrite --cursor 16 --format json -- Buy milk @dev @@"))
4907 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4930:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4928 | 
4929 |         XCTAssertEqual(model.plainDraft, "Buy milk @dev @@ and keep typing")
4930 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4931 |         XCTAssertTrue(record.contains("argv=capture-rewrite --cursor 16 --format json -- Buy milk @dev @@"))
4932 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4964:20: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4962 |         model.editorTextDidChange(cursorUTF8Offset: model.plainDraft.utf8.count)
4963 |         await waitUntil {
4964 |             ((try? String(contentsOf: recordURL)) ?? "").contains("argv=capture-parse")
     |                    `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4965 |         }
4966 | 

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4970:20: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4968 |         model.editorTextDidChange(cursorUTF8Offset: model.plainDraft.utf8.count)
4969 |         await waitUntil {
4970 |             ((try? String(contentsOf: recordURL)) ?? "").contains("Buy milk @dev @@@")
     |                    `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4971 |         }
4972 | 

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4973:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4971 |         }
4972 | 
4973 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
4974 |         XCTAssertFalse(record.contains("capture-rewrite"))
4975 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5009:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5007 | 
5008 |         XCTAssertNil(model.completionResponse)
5009 |         var record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5010 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 1)
5011 |         XCTAssertTrue(

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5026:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5024 |             CaptureRange(start: 6, end: 16)
5025 |         )
5026 |         record = try String(contentsOf: recordURL)
     |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5027 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-complete").count - 1, 2)
5028 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5054:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5052 |         XCTAssertEqual(model.collapsedSelectionUTF8Offset(), "prefix [[AI".utf8.count)
5053 |         XCTAssertEqual(model.statusText, "Link completion warning: skipped unreadable note")
5054 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5055 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 11 --format json -- prefix [[AI suffix"))
5056 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5135:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5133 |         XCTAssertEqual(model.completionResponse?.replacement, CaptureRange(start: 6, end: 8))
5134 |         XCTAssertEqual(model.completionResponse?.candidates.first?.route, "mac_inbox")
5135 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5136 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- idea @ma^new-id"))
5137 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- idea @ma^new-id"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5172:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5170 |         XCTAssertEqual(model.completionResponse?.replacement, CaptureRange(start: 6, end: 8))
5171 |         XCTAssertEqual(model.completionResponse?.candidates.first?.route, "mac_inbox")
5172 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5173 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- idea @ma"))
5174 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- idea @ma"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5210:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5208 |         XCTAssertEqual(model.completionResponse?.replacement, CaptureRange(start: 2, end: 4))
5209 |         XCTAssertEqual(model.completionResponse?.candidates.first?.route, "mac_inbox")
5210 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5211 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- \(draft)"))
5212 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- \(draft)"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5313:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5311 |         XCTAssertEqual(preview.blockID, "new-id")
5312 |         XCTAssertNil(preview.dayFile)
5313 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5314 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- idea @mac_inbox^new-id"))
5315 |         XCTAssertTrue(record.contains("capture-complete"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5340:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5338 | 
5339 |         XCTAssertNil(model.completionResponse)
5340 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5341 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- prefix [[AI suffix"))
5342 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- prefix [[AI suffix"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5373:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5371 |         XCTAssertEqual(model.lastSuccess?.blockID, "parent-id")
5372 | 
5373 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5374 |         XCTAssertTrue(record.contains("argv=capture --format json --refuse-override -- Follow up @file^new-id"))
5375 |         XCTAssertTrue(record.contains("argv=capture --format json --refuse-override -- Add context @file+parent-id"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5436:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5434 |         XCTAssertEqual(model.completionResponse?.replacement, CaptureRange(start: 11, end: 15))
5435 | 
5436 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5437 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- Add context @file+parent-id"))
5438 |         XCTAssertTrue(record.contains("argv=capture --dry-run --no-clip --format json -- Add context @file+parent-id"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5468:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5466 |         XCTAssertEqual(model.completionResponse?.replacement, CaptureRange(start: 1, end: 1))
5467 |         XCTAssertEqual(model.completionResponse?.candidates.first?.route, "file")
5468 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5469 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- @"))
5470 |         XCTAssertFalse(record.contains("capture-complete"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5498:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5496 |         XCTAssertEqual(model.completionResponse?.replacement, CaptureRange(start: 1, end: 3))
5497 |         XCTAssertEqual(model.completionResponse?.candidates.map(\.route), ["file"])
5498 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5499 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- @fi"))
5500 |         XCTAssertFalse(record.contains("capture-complete"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5527:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5525 |         XCTAssertEqual(model.completionResponse?.replacement, CaptureRange(start: 1, end: 3))
5526 |         XCTAssertEqual(model.completionResponse?.candidates.first?.route, "file")
5527 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5528 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- @fi"))
5529 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 3 --format json -- @fi"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5567:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5565 |         XCTAssertEqual(model.plainDraft, "@file+goog-exit")
5566 |         XCTAssertNil(model.completionResponse)
5567 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5568 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 6 --format json -- @file+"))
5569 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5601:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5599 | 
5600 |         await waitUntil { model.completionResponse?.context == "task" }
5601 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5602 |         XCTAssertTrue(
5603 |             record.contains("argv=capture-complete --all-tasks --cursor 16 --format json -- Call bank @cash+")

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5638:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5636 | 
5637 |         await waitUntil { model.completionResponse?.context == "task" }
5638 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5639 |         XCTAssertTrue(
5640 |             record.contains("argv=capture-complete --all-tasks --cursor 16 --format json -- Call bank @Cash+")

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5678:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5676 | 
5677 |         await waitUntil { model.completionResponse?.context == "task" }
5678 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5679 |         XCTAssertTrue(
5680 |             record.contains("argv=capture-complete --all-tasks --cursor 17 --format json -- Add note @design+")

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5793:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5791 | 
5792 |         await waitUntil { model.completionResponse?.context == "task" }
5793 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5794 |         XCTAssertTrue(
5795 |             record.contains(

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5830:32: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5828 | 
5829 |         await waitUntil {
5830 |             let record = (try? String(contentsOf: recordURL)) ?? ""
     |                                `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5831 |             return record.contains("argv=capture-complete --all-tasks --cursor 16 --format json -- Call bank @Cash+")
5832 |         }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5834:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5832 |         }
5833 | 
5834 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5835 |         XCTAssertFalse(record.contains("argv=capture-complete --all-tasks --cursor 15"))
5836 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5867:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5865 | 
5866 |         XCTAssertEqual(model.completionResponse?.candidates.first?.route, "mac_inbox")
5867 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5868 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 8 --format json -- idea @ma"))
5869 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5898:32: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5896 |         model.editorTextDidChange(cursorUTF8Offset: model.plainDraft.utf8.count)
5897 |         await waitUntil {
5898 |             let record = (try? String(contentsOf: recordURL)) ?? ""
     |                                `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5899 |             return record.contains("argv=capture-complete --all-tasks --cursor 16 --format json -- Call bank @Cash+")
5900 |         }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5902:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5900 |         }
5901 | 
5902 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5903 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- Call bank @Cash+"))
5904 |         XCTAssertTrue(

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5938:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5936 |         XCTAssertEqual(model.completionResponse?.candidates.first?.blockID, "goog-exit")
5937 |         XCTAssertTrue(model.completionVisible)
5938 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5939 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 15 --format json -- note @Cash+goog"))
5940 | 

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5980:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5978 |         XCTAssertEqual(model.completionResponse?.candidates.first?.blockID, "bar")
5979 |         XCTAssertEqual(model.completionResponse?.candidates.first?.childCount, 2)
5980 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
5981 |         XCTAssertTrue(
5982 |             record.contains(

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6022:32: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6020 |                 return false
6021 |             }
6022 |             let record = (try? String(contentsOf: recordURL)) ?? ""
     |                                `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6023 |             return record.contains("argv=capture-parse --format json -- jot idea #")
6024 |                 && record.contains("argv=capture --dry-run --no-clip --format json -- jot idea #")

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6032:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6030 |         XCTAssertNil(model.completionResponse)
6031 |         XCTAssertFalse(model.completionVisible)
6032 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6033 |         XCTAssertFalse(record.contains("capture-complete"))
6034 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6054:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6052 |         XCTAssertTrue(model.completionVisible)
6053 |         XCTAssertEqual(model.completionResponse?.candidates.first?.title, "Ideas")
6054 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6055 |         XCTAssertTrue(
6056 |             record.contains(

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6203:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6201 |         XCTAssertEqual(livePreview.normalizedCaptures.map(\.kind), ["task", "sub_bullet"])
6202 | 
6203 |         var record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6204 |         XCTAssertTrue(
6205 |             record.contains("argv=capture-complete --all-tasks --cursor 43 --format json -- ")

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6229:22: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6227 |         XCTAssertEqual(model.lastSuccessResults.map(\.text), ["Plan café", "File follow-up"])
6228 | 
6229 |         record = try String(contentsOf: recordURL)
     |                      `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6230 |         XCTAssertEqual(
6231 |             record.components(separatedBy: "argv=capture --format json --dry-run -- ").count - 1,

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6301:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6299 |         XCTAssertEqual(focusEvents.last?.cursor, "note @Cash+new-id".utf8.count)
6300 |         XCTAssertFalse(model.editorInputLocked)
6301 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6302 |         XCTAssertTrue(
6303 |             record.contains("argv=capture-task-id --route cash --task-ref 8:missingidea --block-id new-id --format json")

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6530:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6528 |             return false
6529 |         }
6530 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6531 |         XCTAssertFalse(record.contains("capture-pomodoro-name"))
6532 |         XCTAssertTrue(record.contains("argv=capture-parse --format json -- "))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6573:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6571 |             return false
6572 |         }
6573 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6574 |         XCTAssertFalse(record.contains("capture-pomodoro-name"))
6575 |         XCTAssertTrue(record.contains(accepted))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6660:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6658 |                 && model.pomodoroNamePrompt?.suggestionsLoading == false
6659 |         }
6660 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6661 |         XCTAssertTrue(record.contains("argv=themes list --format json --limit 5"))
6662 |         XCTAssertTrue(record.contains("argv=themes list --format json --limit 12 --query BOOKS"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6710:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6708 |                 && model.temporarilyHiddenThemeKey == nil
6709 |         }
6710 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6711 |         XCTAssertTrue(record.contains("argv=themes hide BOOKS --via bob-mac-capture --format json"))
6712 |         XCTAssertTrue(record.contains("argv=themes unhide BOOKS --via bob-mac-capture --format json"))

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6767:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6765 |         XCTAssertFalse(model.editorInputLocked)
6766 |         XCTAssertEqual(model.statusText, "Named DEEP WORK in 2026/20260828.md")
6767 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6768 |         XCTAssertTrue(
6769 |             record.contains(

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6994:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6992 |         await waitUntil { model.completionResponse?.context == "wikilink_note" }
6993 | 
6994 |         let record = try String(contentsOf: recordURL)
     |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
6995 |         XCTAssertTrue(record.contains("argv=capture-complete --all-tasks --cursor 9 --format json -- prefix [[AI suffix"))
6996 |     }

Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7267:28: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
7265 |         }
7266 | 
7267 |         let record = (try? String(contentsOf: recordURL)) ?? ""
     |                            `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
7268 |         return record.contains("argv=capture-parse --format json -- \(draft)")
7269 |             && record.contains("argv=capture --dry-run --no-clip --format json -- \(draft)")

Tests/BobMacCaptureTests/CaptureTemplateStartTests.swift:136:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
134 |         XCTAssertNil(model.completionResponse)
135 |         XCTAssertFalse(model.completionVisible)
136 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
137 |         XCTAssertTrue(record.contains("argv=capture-rewrite --cursor 3 --format json -- @@@"))
138 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-rewrite").count - 1, 1)

Tests/BobMacCaptureTests/CaptureTemplateStartTests.swift:198:26: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
196 | 
197 |         XCTAssertEqual(textView.string, "@@")
198 |         let record = try String(contentsOf: recordURL)
    |                          `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
199 |         XCTAssertEqual(record.components(separatedBy: "argv=capture-rewrite").count - 1, 1)
200 |     }

Tests/BobMacCaptureTests/CaptureTemplateStartTests.swift:284:19: warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
282 |         typeAt(into: textView, model: model)
283 |         await waitUntil {
284 |             (try? String(contentsOf: recordURL))?.contains("argv=capture-rewrite") == true
    |                   `- warning: 'init(contentsOf:)' was deprecated in macOS 15: Use `init(contentsOf:encoding:)` instead [#DeprecatedDeclaration]
285 |         }
286 |         XCTAssertEqual(model.plainDraft, "@@@")

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
PASS BobMacCaptureInstallHelperTests
PASS CaptureCoreTests
PASS RefsCoreTests
Type-check only: macOS test targets were checked against a stub; CI still runs the tests.
error: recipe `typecheck-tests` failed on line 30 with exit code 1
TYPECHECK_TESTS_STATUS=1
failed  exit=1  duration=288644ms

