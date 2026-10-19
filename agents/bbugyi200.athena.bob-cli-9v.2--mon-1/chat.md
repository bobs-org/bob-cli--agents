# Chat History - ace-run (bob-cli-9v.2--mon-1)

- **TIMESTAMP:** 2026-10-19 13:53:24 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-9v.2--mon-1

## Prompt

sase monitor start --command 'NEWDIR=/tmp/bobmac-bigpanel.fix1; ssh -o BatchMode=yes mac "rm -rf $NEWDIR" && rsync -az --delete --exclude .build --exclude .git sase/repos/linked/bob-mac-capture/ mac:$NEWDIR/ && ssh -o BatchMode=yes mac "cd $NEWDIR && ./Scripts/bundle.sh && just typecheck-tests" && ssh -o BatchMode=yes mac "rm -rf /tmp/bobmac-bigpanel.retry && echo OLD_SCRATCH_REMOVED"' --reason 'Mac scratch compile for bead bob-cli-9v.2 after argument-order fix: bundle.sh plus typecheck-tests'

## Response

sase tool run c2d595ee312921803649a5b0889b6830
X11 forwarding request failed on channel 0
X11 forwarding request failed on channel 0
Building for production...
[0/6] Write sources
[3/6] Write swift-version--1AB21518FC5DEDBE.txt
[5/7] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/DependencyPickerPresentation.swift:486:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
484 | /// locator stays searchable.
485 | private struct DependencyPickerIndexEntry: Sendable {
486 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
487 |     let bobIndex: Int
488 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[6/8] Compiling RefsCore RefsCaption.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {

/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
824 |     }
825 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
824 |     }
825 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:76:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |     NSApplication.shared.addSceneRepresentation(representation)
 75 |     settingsSceneRepresentation = representation
 76 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |       representation.environment.openSettings()
 78 |     }
    :
818 |   var activateApplication: () -> Void
819 | 
820 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:271:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
269 |     menu.addItem(redo)
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
273 |     menu.addItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:272:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
273 |     menu.addItem(
274 |       NSMenuItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:281:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     )
280 |     menu.addItem(
281 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     return menu
283 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:475:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |   /// off MainActor state.
474 |   nonisolated static func storedHighlightsAppPath() -> String {
475 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
476 |   }
477 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:555:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
553 |       library: library,
554 |       opener: WorkspaceRefsOpener(),
555 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
556 |       tabs: tabsSession,
557 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:730:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
728 |       return
729 |     }
730 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
731 |   }
732 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:519:21: warning: expression of type 'Bool' is unused [#no-usage]
517 |   private func refreshSnapshotAfterRename() async {
518 |     while let current = snapshotTask {
519 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
520 |     }
521 |     refreshSnapshot(reason: .manual)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:523:21: warning: expression of type 'Bool' is unused [#no-usage]
521 |     refreshSnapshot(reason: .manual)
522 |     while let current = snapshotTask {
523 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
524 |     }
525 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:780:21: warning: expression of type 'Bool' is unused [#no-usage]
778 |   private func runPostScanRefresh() async {
779 |     while let current = snapshotTask {
780 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
781 |       if snapshotTask == nil {
782 |         break

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:787:21: warning: expression of type 'Bool' is unused [#no-usage]
785 |     refresh(reason: .scan)
786 |     while let current = snapshotTask {
787 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
788 |       if snapshotTask == nil {
789 |         break

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:851:16: warning: no 'async' operations occur within 'await' expression
849 |           return
850 |         }
851 |         Task { await self?.handleWatcherChange() }
    |                `- warning: no 'async' operations occur within 'await' expression
852 |       },
853 |       onFailure: { [weak self] message in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:854:16: warning: no 'async' operations occur within 'await' expression
852 |       },
853 |       onFailure: { [weak self] message in
854 |         Task { await self?.watcherFailed(message) }
    |                `- warning: no 'async' operations occur within 'await' expression
855 |       }
856 |     )

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsListView.swift:213:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
211 |         // rows report nil, which never clears the current rect.
212 |         .onGeometryChange(for: CGRect?.self) { proxy in
213 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
214 |             ? proxy.frame(in: .named("refsPanel")) : nil
215 |         } action: { rect in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:38: note: property declared here
 287 |     return tabsFilter && tabsListing?.tabs[id] != nil
 288 |   }
 289 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 290 |     didSet {
 291 |       if oldValue != selectedID {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsListView.swift:251:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
249 |       .transition(removalTransition)
250 |       .onGeometryChange(for: CGRect?.self) { proxy in
251 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
252 |           ? proxy.frame(in: .named("refsPanel")) : nil
253 |       } action: { rect in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:38: note: property declared here
 287 |     return tabsFilter && tabsListing?.tabs[id] != nil
 288 |   }
 289 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 290 |     didSet {
 291 |       if oldValue != selectedID {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:183:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 181 |     completion: @escaping (Error?) -> Void
 182 |   ) {
 183 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 184 |     configuration.activates = true
 185 |     NSWorkspace.shared.open(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:206:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 204 | 
 205 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 206 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 207 |     configuration.activates = true
 208 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:561:14: warning: no 'async' operations occur within 'await' expression
 559 |     }.store(in: &subscriptions)
 560 |     let itemsSubscription = library.$items.sink { [weak self] _ in
 561 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 562 |     }
 563 |     let signalsSubscription = library.$signals.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:564:14: warning: no 'async' operations occur within 'await' expression
 562 |     }
 563 |     let signalsSubscription = library.$signals.sink { [weak self] _ in
 564 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 565 |     }
 566 |     itemsSubscription.store(in: &subscriptions)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:569:14: warning: no 'async' operations occur within 'await' expression
 567 |     signalsSubscription.store(in: &subscriptions)
 568 |     library.$todayRefreshGeneration.sink { [weak self] _ in
 569 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 570 |     }.store(in: &subscriptions)
 571 |     library.$scanState.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:572:14: warning: no 'async' operations occur within 'await' expression
 570 |     }.store(in: &subscriptions)
 571 |     library.$scanState.sink { [weak self] _ in
 572 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 573 |     }.store(in: &subscriptions)
 574 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:575:14: warning: no 'async' operations occur within 'await' expression
 573 |     }.store(in: &subscriptions)
 574 |     library.$refreshState.sink { [weak self] _ in
 575 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 576 |     }.store(in: &subscriptions)
 577 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2732:7: warning: result of call to 'openSelected' is unused [#no-usage]
2730 |       openWithDefaultApp(item)
2731 |     case .note, .reveal:
2732 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2733 |     }
2734 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2764:9: warning: no 'async' operations occur within 'await' expression
2762 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
2763 |       Task {
2764 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
2765 |       }
2766 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2791:9: warning: no 'async' operations occur within 'await' expression
2789 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
2790 |       Task {
2791 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
2792 |       }
2793 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2849:9: warning: no 'async' operations occur within 'await' expression
2847 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
2848 |       Task {
2849 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
2850 |           itemID: item.id,
2851 |           title: item.title.text,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2880:9: warning: no 'async' operations occur within 'await' expression
2878 |     opener.openWithDefaultApp(pdf) { [weak self] error in
2879 |       Task {
2880 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
2881 |           itemID: item.id,
2882 |           title: item.title.text,

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[7/9] Write Objects.LinkFileList
[8/9] Linking BobMacCapture
Build of product 'BobMacCapture' complete! (146.35s)
/tmp/bobmac-bigpanel.fix1/.build/bundle/Bob Mac Capture.app
Building for debugging...
[0/18] Write sources
[5/18] Write BobMacCapture-entitlement.plist
[5/18] Write BobMacCaptureInstallHelper-entitlement.plist
[7/18] Write refs-rank-entitlement.plist
[8/18] Write swift-version--1AB21518FC5DEDBE.txt
/tmp/bobmac-bigpanel.fix1/.build/bundle/Bob Mac Capture.app/Contents/MacOS/BobMacCapture: replacing existing signature
/tmp/bobmac-bigpanel.fix1/.build/bundle/Bob Mac Capture.app: replacing existing signature
./Scripts/typecheck-tests.sh
[10/73] Emitting module CaptureCore
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/DependencyPickerPresentation.swift:486:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
484 | /// locator stays searchable.
485 | private struct DependencyPickerIndexEntry: Sendable {
486 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
487 |     let bobIndex: Int
488 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[11/73] Compiling CaptureCore CaptureOpenHintPresentation.swift
[12/73] Compiling CaptureCore CaptureOpenPlan.swift
[13/73] Compiling CaptureCore CapturePanelPlacement.swift
[14/73] Compiling CaptureCore CapturePickerHelpers.swift
[15/73] Compiling CaptureCore CapturePickerPresentation.swift
[16/73] Compiling CaptureCore CapturePlanBudgetPresentation.swift
[17/73] Compiling CaptureCore CapturePomodoroAdjustPresentation.swift
[18/73] Compiling CaptureCore CapturePomodoroBlockPresentation.swift
[19/73] Compiling CaptureCore CapturePomodoroClosePresentation.swift
[20/73] Compiling CaptureCore CapturePomodoroLineTokens.swift
[21/73] Compiling CaptureCore CapturePomodoroLinkPresentation.swift
[22/73] Compiling CaptureCore CapturePomodoroResetPresentation.swift
[23/73] Compiling CaptureCore CapturePomodoroShiftPresentation.swift
[24/73] Compiling CaptureCore CapturePomodoroStartPresentation.swift
[25/73] Compiling CaptureCore CaptureProjectNotePresentation.swift
[26/73] Compiling CaptureCore CaptureRefFileUnder.swift
[27/73] Compiling CaptureCore CaptureRefPresentation.swift
[28/73] Compiling CaptureCore CaptureRelationshipCopy.swift
[29/73] Compiling CaptureCore CaptureRelationshipPresentation.swift
[30/73] Compiling CaptureCore CaptureSavedTemplates.swift
[31/73] Compiling CaptureCore CaptureSubBulletPresentation.swift
[32/73] Compiling CaptureCore CaptureSuccessorPresentation.swift
[33/73] Compiling CaptureCore CaptureTargetsCache.swift
[34/73] Compiling CaptureCore CaptureTaskBlockPresentation.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/DependencyPickerPresentation.swift:486:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
484 | /// locator stays searchable.
485 | private struct DependencyPickerIndexEntry: Sendable {
486 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
487 |     let bobIndex: Int
488 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[35/73] Compiling CaptureCore CaptureTaskCompletePresentation.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/DependencyPickerPresentation.swift:486:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
484 | /// locator stays searchable.
485 | private struct DependencyPickerIndexEntry: Sendable {
486 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
487 |     let bobIndex: Int
488 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[36/73] Compiling CaptureCore CaptureTextRanges.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/DependencyPickerPresentation.swift:486:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
484 | /// locator stays searchable.
485 | private struct DependencyPickerIndexEntry: Sendable {
486 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
487 |     let bobIndex: Int
488 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[37/73] Compiling CaptureCore CaptureTodayPomodoroGoto.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/DependencyPickerPresentation.swift:486:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
484 | /// locator stays searchable.
485 | private struct DependencyPickerIndexEntry: Sendable {
486 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
487 |     let bobIndex: Int
488 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[38/73] Compiling CaptureCore CaptureTogglePresentation.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/DependencyPickerPresentation.swift:486:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
484 | /// locator stays searchable.
485 | private struct DependencyPickerIndexEntry: Sendable {
486 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
487 |     let bobIndex: Int
488 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[39/73] Compiling CaptureCore CompletionRowContent.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/DependencyPickerPresentation.swift:486:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
484 | /// locator stays searchable.
485 | private struct DependencyPickerIndexEntry: Sendable {
486 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
487 |     let bobIndex: Int
488 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[40/73] Compiling CaptureCore DependencyPickerPresentation.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/DependencyPickerPresentation.swift:486:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
484 | /// locator stays searchable.
485 | private struct DependencyPickerIndexEntry: Sendable {
486 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
487 |     let bobIndex: Int
488 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[41/73] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[42/73] Compiling CaptureCore BlockIDPickerIndex.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[43/73] Compiling CaptureCore BlockIDRules.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[44/73] Compiling CaptureCore BobEnvironment.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[45/73] Compiling CaptureCore BobErrors.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[46/73] Compiling CaptureCore BobExecutableResolver.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[47/73] Compiling CaptureCore BobMacCaptureLaunchContext.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[48/73] Compiling CaptureCore BobProcessClient.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[49/80] Compiling CaptureCore CanceledDraftStashStore.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[50/80] Compiling CaptureCore CaptureAgendaFitPlanner.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[51/80] Compiling CaptureCore CaptureAgendaHold.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[52/80] Compiling CaptureCore CaptureAgendaInlineText.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[53/80] Compiling CaptureCore CaptureAgendaLayout.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[54/80] Compiling CaptureCore CaptureAgendaModels.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[55/80] Compiling CaptureCore CaptureAgendaPresentation.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[56/80] Compiling CaptureCore CaptureAgendaRefreshFilter.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[57/80] Compiling CaptureCore FuzzyMatcher.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[58/80] Compiling CaptureCore ObsidianOpenURL.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[59/80] Compiling CaptureCore ParentTaskPickerPresentation.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[60/80] Compiling CaptureCore PomodoroHomes.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[61/80] Compiling CaptureCore TaskCompletePickerPresentation.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[62/80] Compiling CaptureCore TaskDisplayText.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[63/80] Compiling CaptureCore TaskLinkPickerPresentation.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bobmac-bigpanel.fix1/Sources/CaptureCore/CaptureModels.swift:5740:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5738 | }
5739 | 
5740 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
5741 |   public let replacement: String
5742 |   public let route: String?
[64/80] Compiling CaptureCore CaptureAgendaRefreshState.swift
[65/80] Compiling CaptureCore CaptureAgendaVisibility.swift
[66/80] Compiling CaptureCore CaptureBlockDiffRow.swift
[67/80] Compiling CaptureCore CaptureCloseTaskCommaAssist.swift
[68/80] Compiling CaptureCore CaptureCloseTaskCommaProvenance.swift
[69/80] Compiling CaptureCore CaptureEditWrite.swift
[70/80] Compiling CaptureCore CaptureLinkGuardPresentation.swift
[71/80] Compiling CaptureCore CaptureModels.swift
[72/107] Compiling RefsCore RefsNew.swift
[73/107] Compiling RefsCore RefsNewest.swift
[74/107] Compiling RefsCore RefsPanelGeometry.swift
[75/110] Compiling RefsCore RefsFetching.swift
[76/110] Compiling RefsCore RefsHighlightPicker.swift
[77/110] Compiling RefsCore RefsHighlightsTabs.swift
[78/110] Emitting module RefsCore
/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[79/110] Compiling RefsCore RefsTabsRanking.swift
[80/110] Compiling RefsCore RefsToday.swift
[81/110] Compiling RefsCore RefsTodayLinkCard.swift
[82/110] Compiling RefsCore RefsTodayLinkModels.swift
[83/110] Compiling RefsCore RefsTodayLinkPresentation.swift
[84/110] Compiling RefsCore RefsWatcherRelevance.swift
[85/110] Compiling RefsCore RefsInspector.swift
[86/110] Compiling RefsCore RefsInspectorImages.swift
[87/110] Compiling RefsCore RefsModel.swift
[88/110] Compiling RefsCore RefsCaption.swift
[89/110] Compiling RefsCore RefsCopy.swift
[90/110] Compiling RefsCore RefsDecoding.swift
[91/110] Compiling RefsCore RefsSelection.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[92/110] Compiling RefsCore RefsStores.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[93/110] Compiling RefsCore RefsTabClose.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[94/110] Compiling RefsCore RefsRanking.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {
[95/110] Compiling RefsCore RefsRename.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {
[96/110] Compiling RefsCore RefsScan.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {
[97/171] Compiling refs_rank main.swift
[98/171] Emitting module refs_rank
[98/171] Write Objects.LinkFileList
[99/171] Linking refs-rank
[100/171] Applying refs-rank
[102/171] Emitting module BobMacCaptureInstallHelper
[103/171] Compiling BobMacCaptureInstallHelper InstallRelauncher.swift
[104/171] Compiling BobMacCaptureInstallHelper InstallHelperArguments.swift
[105/171] Compiling BobMacCaptureInstallHelper InstallHelperError.swift
[106/171] Compiling BobMacCaptureInstallHelper BobMacCaptureInstallHelperMain.swift
[106/171] Write Objects.LinkFileList
[107/171] Linking BobMacCaptureInstallHelper
[108/171] Applying BobMacCaptureInstallHelper
[110/171] Emitting module BobMacCapture
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
824 |     }
825 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
824 |     }
825 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[111/179] Compiling BobMacCapture CaptureSnippetResolver.swift
[112/179] Compiling BobMacCapture HighlightsTakeover.swift
[113/179] Compiling BobMacCapture HotKeyRegistry.swift
[114/179] Compiling BobMacCapture NotificationService.swift
[115/179] Compiling BobMacCapture PlainTextPaste.swift
[116/179] Compiling BobMacCapture PomodoroBlockView.swift
[117/179] Compiling BobMacCapture PomodoroHomeColor.swift
[118/179] Compiling BobMacCapture PomodoroNameField.swift
[119/179] Compiling BobMacCapture RefsHotkeyRegistration.swift
[120/179] Compiling BobMacCapture SavedTemplateShelf.swift
[121/179] Compiling BobMacCapture SettingsView.swift
[122/179] Compiling BobMacCapture Signposts.swift
[123/179] Compiling BobMacCapture StatusItemController.swift
[124/179] Compiling BobMacCapture StatusItemGlyph.swift
[125/179] Compiling BobMacCapture TaskBlockView.swift
[126/179] Compiling BobMacCapture VaultTargetWatcher.swift
[127/179] Compiling BobMacCapture AXHighlightsTabsReader.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[128/179] Compiling BobMacCapture RefsActionsMenu.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[129/179] Compiling BobMacCapture RefsCopyCardView.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[130/179] Compiling BobMacCapture RefsCopyHUD.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[131/179] Compiling BobMacCapture RefsFooter.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[132/179] Compiling BobMacCapture RefsInspectorLoader.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[133/179] Compiling BobMacCapture RefsInspectorScroll.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[134/179] Compiling BobMacCapture RefsInspectorView.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 
[135/179] Compiling BobMacCapture RefsKeyRouter.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:519:21: warning: expression of type 'Bool' is unused [#no-usage]
517 |   private func refreshSnapshotAfterRename() async {
518 |     while let current = snapshotTask {
519 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
520 |     }
521 |     refreshSnapshot(reason: .manual)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:523:21: warning: expression of type 'Bool' is unused [#no-usage]
521 |     refreshSnapshot(reason: .manual)
522 |     while let current = snapshotTask {
523 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
524 |     }
525 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:780:21: warning: expression of type 'Bool' is unused [#no-usage]
778 |   private func runPostScanRefresh() async {
779 |     while let current = snapshotTask {
780 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
781 |       if snapshotTask == nil {
782 |         break

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:787:21: warning: expression of type 'Bool' is unused [#no-usage]
785 |     refresh(reason: .scan)
786 |     while let current = snapshotTask {
787 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
788 |       if snapshotTask == nil {
789 |         break

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:851:16: warning: no 'async' operations occur within 'await' expression
849 |           return
850 |         }
851 |         Task { await self?.handleWatcherChange() }
    |                `- warning: no 'async' operations occur within 'await' expression
852 |       },
853 |       onFailure: { [weak self] message in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:854:16: warning: no 'async' operations occur within 'await' expression
852 |       },
853 |       onFailure: { [weak self] message in
854 |         Task { await self?.watcherFailed(message) }
    |                `- warning: no 'async' operations occur within 'await' expression
855 |       }
856 |     )

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsListView.swift:213:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
211 |         // rows report nil, which never clears the current rect.
212 |         .onGeometryChange(for: CGRect?.self) { proxy in
213 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
214 |             ? proxy.frame(in: .named("refsPanel")) : nil
215 |         } action: { rect in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:38: note: property declared here
 287 |     return tabsFilter && tabsListing?.tabs[id] != nil
 288 |   }
 289 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 290 |     didSet {
 291 |       if oldValue != selectedID {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsListView.swift:251:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
249 |       .transition(removalTransition)
250 |       .onGeometryChange(for: CGRect?.self) { proxy in
251 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
252 |           ? proxy.frame(in: .named("refsPanel")) : nil
253 |       } action: { rect in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:38: note: property declared here
 287 |     return tabsFilter && tabsListing?.tabs[id] != nil
 288 |   }
 289 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 290 |     didSet {
 291 |       if oldValue != selectedID {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:183:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 181 |     completion: @escaping (Error?) -> Void
 182 |   ) {
 183 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 184 |     configuration.activates = true
 185 |     NSWorkspace.shared.open(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:206:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 204 | 
 205 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 206 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 207 |     configuration.activates = true
 208 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:561:14: warning: no 'async' operations occur within 'await' expression
 559 |     }.store(in: &subscriptions)
 560 |     let itemsSubscription = library.$items.sink { [weak self] _ in
 561 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 562 |     }
 563 |     let signalsSubscription = library.$signals.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:564:14: warning: no 'async' operations occur within 'await' expression
 562 |     }
 563 |     let signalsSubscription = library.$signals.sink { [weak self] _ in
 564 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 565 |     }
 566 |     itemsSubscription.store(in: &subscriptions)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:569:14: warning: no 'async' operations occur within 'await' expression
 567 |     signalsSubscription.store(in: &subscriptions)
 568 |     library.$todayRefreshGeneration.sink { [weak self] _ in
 569 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 570 |     }.store(in: &subscriptions)
 571 |     library.$scanState.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:572:14: warning: no 'async' operations occur within 'await' expression
 570 |     }.store(in: &subscriptions)
 571 |     library.$scanState.sink { [weak self] _ in
 572 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 573 |     }.store(in: &subscriptions)
 574 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:575:14: warning: no 'async' operations occur within 'await' expression
 573 |     }.store(in: &subscriptions)
 574 |     library.$refreshState.sink { [weak self] _ in
 575 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 576 |     }.store(in: &subscriptions)
 577 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2732:7: warning: result of call to 'openSelected' is unused [#no-usage]
2730 |       openWithDefaultApp(item)
2731 |     case .note, .reveal:
2732 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2733 |     }
2734 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2764:9: warning: no 'async' operations occur within 'await' expression
2762 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
2763 |       Task {
2764 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
2765 |       }
2766 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2791:9: warning: no 'async' operations occur within 'await' expression
2789 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
2790 |       Task {
2791 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
2792 |       }
2793 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2849:9: warning: no 'async' operations occur within 'await' expression
2847 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
2848 |       Task {
2849 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
2850 |           itemID: item.id,
2851 |           title: item.title.text,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2880:9: warning: no 'async' operations occur within 'await' expression
2878 |     opener.openWithDefaultApp(pdf) { [weak self] error in
2879 |       Task {
2880 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
2881 |           itemID: item.id,
2882 |           title: item.title.text,
[136/179] Compiling BobMacCapture RefsLibrary.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:519:21: warning: expression of type 'Bool' is unused [#no-usage]
517 |   private func refreshSnapshotAfterRename() async {
518 |     while let current = snapshotTask {
519 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
520 |     }
521 |     refreshSnapshot(reason: .manual)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:523:21: warning: expression of type 'Bool' is unused [#no-usage]
521 |     refreshSnapshot(reason: .manual)
522 |     while let current = snapshotTask {
523 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
524 |     }
525 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:780:21: warning: expression of type 'Bool' is unused [#no-usage]
778 |   private func runPostScanRefresh() async {
779 |     while let current = snapshotTask {
780 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
781 |       if snapshotTask == nil {
782 |         break

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:787:21: warning: expression of type 'Bool' is unused [#no-usage]
785 |     refresh(reason: .scan)
786 |     while let current = snapshotTask {
787 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
788 |       if snapshotTask == nil {
789 |         break

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:851:16: warning: no 'async' operations occur within 'await' expression
849 |           return
850 |         }
851 |         Task { await self?.handleWatcherChange() }
    |                `- warning: no 'async' operations occur within 'await' expression
852 |       },
853 |       onFailure: { [weak self] message in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:854:16: warning: no 'async' operations occur within 'await' expression
852 |       },
853 |       onFailure: { [weak self] message in
854 |         Task { await self?.watcherFailed(message) }
    |                `- warning: no 'async' operations occur within 'await' expression
855 |       }
856 |     )

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsListView.swift:213:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
211 |         // rows report nil, which never clears the current rect.
212 |         .onGeometryChange(for: CGRect?.self) { proxy in
213 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
214 |             ? proxy.frame(in: .named("refsPanel")) : nil
215 |         } action: { rect in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:38: note: property declared here
 287 |     return tabsFilter && tabsListing?.tabs[id] != nil
 288 |   }
 289 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 290 |     didSet {
 291 |       if oldValue != selectedID {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsListView.swift:251:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
249 |       .transition(removalTransition)
250 |       .onGeometryChange(for: CGRect?.self) { proxy in
251 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
252 |           ? proxy.frame(in: .named("refsPanel")) : nil
253 |       } action: { rect in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:38: note: property declared here
 287 |     return tabsFilter && tabsListing?.tabs[id] != nil
 288 |   }
 289 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 290 |     didSet {
 291 |       if oldValue != selectedID {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:183:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 181 |     completion: @escaping (Error?) -> Void
 182 |   ) {
 183 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 184 |     configuration.activates = true
 185 |     NSWorkspace.shared.open(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:206:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 204 | 
 205 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 206 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 207 |     configuration.activates = true
 208 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:561:14: warning: no 'async' operations occur within 'await' expression
 559 |     }.store(in: &subscriptions)
 560 |     let itemsSubscription = library.$items.sink { [weak self] _ in
 561 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 562 |     }
 563 |     let signalsSubscription = library.$signals.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:564:14: warning: no 'async' operations occur within 'await' expression
 562 |     }
 563 |     let signalsSubscription = library.$signals.sink { [weak self] _ in
 564 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 565 |     }
 566 |     itemsSubscription.store(in: &subscriptions)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:569:14: warning: no 'async' operations occur within 'await' expression
 567 |     signalsSubscription.store(in: &subscriptions)
 568 |     library.$todayRefreshGeneration.sink { [weak self] _ in
 569 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 570 |     }.store(in: &subscriptions)
 571 |     library.$scanState.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:572:14: warning: no 'async' operations occur within 'await' expression
 570 |     }.store(in: &subscriptions)
 571 |     library.$scanState.sink { [weak self] _ in
 572 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 573 |     }.store(in: &subscriptions)
 574 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:575:14: warning: no 'async' operations occur within 'await' expression
 573 |     }.store(in: &subscriptions)
 574 |     library.$refreshState.sink { [weak self] _ in
 575 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 576 |     }.store(in: &subscriptions)
 577 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2732:7: warning: result of call to 'openSelected' is unused [#no-usage]
2730 |       openWithDefaultApp(item)
2731 |     case .note, .reveal:
2732 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2733 |     }
2734 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2764:9: warning: no 'async' operations occur within 'await' expression
2762 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
2763 |       Task {
2764 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
2765 |       }
2766 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2791:9: warning: no 'async' operations occur within 'await' expression
2789 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
2790 |       Task {
2791 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
2792 |       }
2793 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2849:9: warning: no 'async' operations occur within 'await' expression
2847 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
2848 |       Task {
2849 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
2850 |           itemID: item.id,
2851 |           title: item.title.text,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2880:9: warning: no 'async' operations occur within 'await' expression
2878 |     opener.openWithDefaultApp(pdf) { [weak self] error in
2879 |       Task {
2880 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
2881 |           itemID: item.id,
2882 |           title: item.title.text,
[137/179] Compiling BobMacCapture RefsListView.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:519:21: warning: expression of type 'Bool' is unused [#no-usage]
517 |   private func refreshSnapshotAfterRename() async {
518 |     while let current = snapshotTask {
519 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
520 |     }
521 |     refreshSnapshot(reason: .manual)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:523:21: warning: expression of type 'Bool' is unused [#no-usage]
521 |     refreshSnapshot(reason: .manual)
522 |     while let current = snapshotTask {
523 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
524 |     }
525 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:780:21: warning: expression of type 'Bool' is unused [#no-usage]
778 |   private func runPostScanRefresh() async {
779 |     while let current = snapshotTask {
780 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
781 |       if snapshotTask == nil {
782 |         break

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:787:21: warning: expression of type 'Bool' is unused [#no-usage]
785 |     refresh(reason: .scan)
786 |     while let current = snapshotTask {
787 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
788 |       if snapshotTask == nil {
789 |         break

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:851:16: warning: no 'async' operations occur within 'await' expression
849 |           return
850 |         }
851 |         Task { await self?.handleWatcherChange() }
    |                `- warning: no 'async' operations occur within 'await' expression
852 |       },
853 |       onFailure: { [weak self] message in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:854:16: warning: no 'async' operations occur within 'await' expression
852 |       },
853 |       onFailure: { [weak self] message in
854 |         Task { await self?.watcherFailed(message) }
    |                `- warning: no 'async' operations occur within 'await' expression
855 |       }
856 |     )

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsListView.swift:213:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
211 |         // rows report nil, which never clears the current rect.
212 |         .onGeometryChange(for: CGRect?.self) { proxy in
213 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
214 |             ? proxy.frame(in: .named("refsPanel")) : nil
215 |         } action: { rect in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:38: note: property declared here
 287 |     return tabsFilter && tabsListing?.tabs[id] != nil
 288 |   }
 289 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 290 |     didSet {
 291 |       if oldValue != selectedID {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsListView.swift:251:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
249 |       .transition(removalTransition)
250 |       .onGeometryChange(for: CGRect?.self) { proxy in
251 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
252 |           ? proxy.frame(in: .named("refsPanel")) : nil
253 |       } action: { rect in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:38: note: property declared here
 287 |     return tabsFilter && tabsListing?.tabs[id] != nil
 288 |   }
 289 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 290 |     didSet {
 291 |       if oldValue != selectedID {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:183:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 181 |     completion: @escaping (Error?) -> Void
 182 |   ) {
 183 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 184 |     configuration.activates = true
 185 |     NSWorkspace.shared.open(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:206:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 204 | 
 205 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 206 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 207 |     configuration.activates = true
 208 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:561:14: warning: no 'async' operations occur within 'await' expression
 559 |     }.store(in: &subscriptions)
 560 |     let itemsSubscription = library.$items.sink { [weak self] _ in
 561 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 562 |     }
 563 |     let signalsSubscription = library.$signals.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:564:14: warning: no 'async' operations occur within 'await' expression
 562 |     }
 563 |     let signalsSubscription = library.$signals.sink { [weak self] _ in
 564 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 565 |     }
 566 |     itemsSubscription.store(in: &subscriptions)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:569:14: warning: no 'async' operations occur within 'await' expression
 567 |     signalsSubscription.store(in: &subscriptions)
 568 |     library.$todayRefreshGeneration.sink { [weak self] _ in
 569 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 570 |     }.store(in: &subscriptions)
 571 |     library.$scanState.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:572:14: warning: no 'async' operations occur within 'await' expression
 570 |     }.store(in: &subscriptions)
 571 |     library.$scanState.sink { [weak self] _ in
 572 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 573 |     }.store(in: &subscriptions)
 574 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:575:14: warning: no 'async' operations occur within 'await' expression
 573 |     }.store(in: &subscriptions)
 574 |     library.$refreshState.sink { [weak self] _ in
 575 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 576 |     }.store(in: &subscriptions)
 577 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2732:7: warning: result of call to 'openSelected' is unused [#no-usage]
2730 |       openWithDefaultApp(item)
2731 |     case .note, .reveal:
2732 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2733 |     }
2734 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2764:9: warning: no 'async' operations occur within 'await' expression
2762 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
2763 |       Task {
2764 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
2765 |       }
2766 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2791:9: warning: no 'async' operations occur within 'await' expression
2789 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
2790 |       Task {
2791 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
2792 |       }
2793 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2849:9: warning: no 'async' operations occur within 'await' expression
2847 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
2848 |       Task {
2849 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
2850 |           itemID: item.id,
2851 |           title: item.title.text,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2880:9: warning: no 'async' operations occur within 'await' expression
2878 |     opener.openWithDefaultApp(pdf) { [weak self] error in
2879 |       Task {
2880 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
2881 |           itemID: item.id,
2882 |           title: item.title.text,
[138/179] Compiling BobMacCapture RefsPanel.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:519:21: warning: expression of type 'Bool' is unused [#no-usage]
517 |   private func refreshSnapshotAfterRename() async {
518 |     while let current = snapshotTask {
519 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
520 |     }
521 |     refreshSnapshot(reason: .manual)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:523:21: warning: expression of type 'Bool' is unused [#no-usage]
521 |     refreshSnapshot(reason: .manual)
522 |     while let current = snapshotTask {
523 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
524 |     }
525 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:780:21: warning: expression of type 'Bool' is unused [#no-usage]
778 |   private func runPostScanRefresh() async {
779 |     while let current = snapshotTask {
780 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
781 |       if snapshotTask == nil {
782 |         break

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:787:21: warning: expression of type 'Bool' is unused [#no-usage]
785 |     refresh(reason: .scan)
786 |     while let current = snapshotTask {
787 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
788 |       if snapshotTask == nil {
789 |         break

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:851:16: warning: no 'async' operations occur within 'await' expression
849 |           return
850 |         }
851 |         Task { await self?.handleWatcherChange() }
    |                `- warning: no 'async' operations occur within 'await' expression
852 |       },
853 |       onFailure: { [weak self] message in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:854:16: warning: no 'async' operations occur within 'await' expression
852 |       },
853 |       onFailure: { [weak self] message in
854 |         Task { await self?.watcherFailed(message) }
    |                `- warning: no 'async' operations occur within 'await' expression
855 |       }
856 |     )

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsListView.swift:213:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
211 |         // rows report nil, which never clears the current rect.
212 |         .onGeometryChange(for: CGRect?.self) { proxy in
213 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
214 |             ? proxy.frame(in: .named("refsPanel")) : nil
215 |         } action: { rect in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:38: note: property declared here
 287 |     return tabsFilter && tabsListing?.tabs[id] != nil
 288 |   }
 289 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 290 |     didSet {
 291 |       if oldValue != selectedID {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsListView.swift:251:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
249 |       .transition(removalTransition)
250 |       .onGeometryChange(for: CGRect?.self) { proxy in
251 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
252 |           ? proxy.frame(in: .named("refsPanel")) : nil
253 |       } action: { rect in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:38: note: property declared here
 287 |     return tabsFilter && tabsListing?.tabs[id] != nil
 288 |   }
 289 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 290 |     didSet {
 291 |       if oldValue != selectedID {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:183:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 181 |     completion: @escaping (Error?) -> Void
 182 |   ) {
 183 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 184 |     configuration.activates = true
 185 |     NSWorkspace.shared.open(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:206:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 204 | 
 205 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 206 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 207 |     configuration.activates = true
 208 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:561:14: warning: no 'async' operations occur within 'await' expression
 559 |     }.store(in: &subscriptions)
 560 |     let itemsSubscription = library.$items.sink { [weak self] _ in
 561 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 562 |     }
 563 |     let signalsSubscription = library.$signals.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:564:14: warning: no 'async' operations occur within 'await' expression
 562 |     }
 563 |     let signalsSubscription = library.$signals.sink { [weak self] _ in
 564 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 565 |     }
 566 |     itemsSubscription.store(in: &subscriptions)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:569:14: warning: no 'async' operations occur within 'await' expression
 567 |     signalsSubscription.store(in: &subscriptions)
 568 |     library.$todayRefreshGeneration.sink { [weak self] _ in
 569 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 570 |     }.store(in: &subscriptions)
 571 |     library.$scanState.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:572:14: warning: no 'async' operations occur within 'await' expression
 570 |     }.store(in: &subscriptions)
 571 |     library.$scanState.sink { [weak self] _ in
 572 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 573 |     }.store(in: &subscriptions)
 574 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:575:14: warning: no 'async' operations occur within 'await' expression
 573 |     }.store(in: &subscriptions)
 574 |     library.$refreshState.sink { [weak self] _ in
 575 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 576 |     }.store(in: &subscriptions)
 577 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2732:7: warning: result of call to 'openSelected' is unused [#no-usage]
2730 |       openWithDefaultApp(item)
2731 |     case .note, .reveal:
2732 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2733 |     }
2734 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2764:9: warning: no 'async' operations occur within 'await' expression
2762 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
2763 |       Task {
2764 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
2765 |       }
2766 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2791:9: warning: no 'async' operations occur within 'await' expression
2789 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
2790 |       Task {
2791 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
2792 |       }
2793 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2849:9: warning: no 'async' operations occur within 'await' expression
2847 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
2848 |       Task {
2849 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
2850 |           itemID: item.id,
2851 |           title: item.title.text,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2880:9: warning: no 'async' operations occur within 'await' expression
2878 |     opener.openWithDefaultApp(pdf) { [weak self] error in
2879 |       Task {
2880 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
2881 |           itemID: item.id,
2882 |           title: item.title.text,
[139/179] Compiling BobMacCapture RefsPanelModel.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:519:21: warning: expression of type 'Bool' is unused [#no-usage]
517 |   private func refreshSnapshotAfterRename() async {
518 |     while let current = snapshotTask {
519 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
520 |     }
521 |     refreshSnapshot(reason: .manual)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:523:21: warning: expression of type 'Bool' is unused [#no-usage]
521 |     refreshSnapshot(reason: .manual)
522 |     while let current = snapshotTask {
523 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
524 |     }
525 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:780:21: warning: expression of type 'Bool' is unused [#no-usage]
778 |   private func runPostScanRefresh() async {
779 |     while let current = snapshotTask {
780 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
781 |       if snapshotTask == nil {
782 |         break

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:787:21: warning: expression of type 'Bool' is unused [#no-usage]
785 |     refresh(reason: .scan)
786 |     while let current = snapshotTask {
787 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
788 |       if snapshotTask == nil {
789 |         break

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:851:16: warning: no 'async' operations occur within 'await' expression
849 |           return
850 |         }
851 |         Task { await self?.handleWatcherChange() }
    |                `- warning: no 'async' operations occur within 'await' expression
852 |       },
853 |       onFailure: { [weak self] message in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:854:16: warning: no 'async' operations occur within 'await' expression
852 |       },
853 |       onFailure: { [weak self] message in
854 |         Task { await self?.watcherFailed(message) }
    |                `- warning: no 'async' operations occur within 'await' expression
855 |       }
856 |     )

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsListView.swift:213:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
211 |         // rows report nil, which never clears the current rect.
212 |         .onGeometryChange(for: CGRect?.self) { proxy in
213 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
214 |             ? proxy.frame(in: .named("refsPanel")) : nil
215 |         } action: { rect in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:38: note: property declared here
 287 |     return tabsFilter && tabsListing?.tabs[id] != nil
 288 |   }
 289 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 290 |     didSet {
 291 |       if oldValue != selectedID {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsListView.swift:251:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
249 |       .transition(removalTransition)
250 |       .onGeometryChange(for: CGRect?.self) { proxy in
251 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
252 |           ? proxy.frame(in: .named("refsPanel")) : nil
253 |       } action: { rect in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:38: note: property declared here
 287 |     return tabsFilter && tabsListing?.tabs[id] != nil
 288 |   }
 289 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 290 |     didSet {
 291 |       if oldValue != selectedID {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:183:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 181 |     completion: @escaping (Error?) -> Void
 182 |   ) {
 183 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 184 |     configuration.activates = true
 185 |     NSWorkspace.shared.open(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:206:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 204 | 
 205 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 206 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 207 |     configuration.activates = true
 208 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:561:14: warning: no 'async' operations occur within 'await' expression
 559 |     }.store(in: &subscriptions)
 560 |     let itemsSubscription = library.$items.sink { [weak self] _ in
 561 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 562 |     }
 563 |     let signalsSubscription = library.$signals.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:564:14: warning: no 'async' operations occur within 'await' expression
 562 |     }
 563 |     let signalsSubscription = library.$signals.sink { [weak self] _ in
 564 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 565 |     }
 566 |     itemsSubscription.store(in: &subscriptions)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:569:14: warning: no 'async' operations occur within 'await' expression
 567 |     signalsSubscription.store(in: &subscriptions)
 568 |     library.$todayRefreshGeneration.sink { [weak self] _ in
 569 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 570 |     }.store(in: &subscriptions)
 571 |     library.$scanState.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:572:14: warning: no 'async' operations occur within 'await' expression
 570 |     }.store(in: &subscriptions)
 571 |     library.$scanState.sink { [weak self] _ in
 572 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 573 |     }.store(in: &subscriptions)
 574 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:575:14: warning: no 'async' operations occur within 'await' expression
 573 |     }.store(in: &subscriptions)
 574 |     library.$refreshState.sink { [weak self] _ in
 575 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 576 |     }.store(in: &subscriptions)
 577 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2732:7: warning: result of call to 'openSelected' is unused [#no-usage]
2730 |       openWithDefaultApp(item)
2731 |     case .note, .reveal:
2732 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2733 |     }
2734 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2764:9: warning: no 'async' operations occur within 'await' expression
2762 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
2763 |       Task {
2764 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
2765 |       }
2766 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2791:9: warning: no 'async' operations occur within 'await' expression
2789 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
2790 |       Task {
2791 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
2792 |       }
2793 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2849:9: warning: no 'async' operations occur within 'await' expression
2847 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
2848 |       Task {
2849 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
2850 |           itemID: item.id,
2851 |           title: item.title.text,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2880:9: warning: no 'async' operations occur within 'await' expression
2878 |     opener.openWithDefaultApp(pdf) { [weak self] error in
2879 |       Task {
2880 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
2881 |           itemID: item.id,
2882 |           title: item.title.text,
[140/179] Compiling BobMacCapture RefsPanelStates.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:519:21: warning: expression of type 'Bool' is unused [#no-usage]
517 |   private func refreshSnapshotAfterRename() async {
518 |     while let current = snapshotTask {
519 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
520 |     }
521 |     refreshSnapshot(reason: .manual)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:523:21: warning: expression of type 'Bool' is unused [#no-usage]
521 |     refreshSnapshot(reason: .manual)
522 |     while let current = snapshotTask {
523 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
524 |     }
525 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:780:21: warning: expression of type 'Bool' is unused [#no-usage]
778 |   private func runPostScanRefresh() async {
779 |     while let current = snapshotTask {
780 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
781 |       if snapshotTask == nil {
782 |         break

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:787:21: warning: expression of type 'Bool' is unused [#no-usage]
785 |     refresh(reason: .scan)
786 |     while let current = snapshotTask {
787 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
788 |       if snapshotTask == nil {
789 |         break

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:851:16: warning: no 'async' operations occur within 'await' expression
849 |           return
850 |         }
851 |         Task { await self?.handleWatcherChange() }
    |                `- warning: no 'async' operations occur within 'await' expression
852 |       },
853 |       onFailure: { [weak self] message in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:854:16: warning: no 'async' operations occur within 'await' expression
852 |       },
853 |       onFailure: { [weak self] message in
854 |         Task { await self?.watcherFailed(message) }
    |                `- warning: no 'async' operations occur within 'await' expression
855 |       }
856 |     )

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsListView.swift:213:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
211 |         // rows report nil, which never clears the current rect.
212 |         .onGeometryChange(for: CGRect?.self) { proxy in
213 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
214 |             ? proxy.frame(in: .named("refsPanel")) : nil
215 |         } action: { rect in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:38: note: property declared here
 287 |     return tabsFilter && tabsListing?.tabs[id] != nil
 288 |   }
 289 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 290 |     didSet {
 291 |       if oldValue != selectedID {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsListView.swift:251:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
249 |       .transition(removalTransition)
250 |       .onGeometryChange(for: CGRect?.self) { proxy in
251 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
252 |           ? proxy.frame(in: .named("refsPanel")) : nil
253 |       } action: { rect in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:38: note: property declared here
 287 |     return tabsFilter && tabsListing?.tabs[id] != nil
 288 |   }
 289 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 290 |     didSet {
 291 |       if oldValue != selectedID {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:183:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 181 |     completion: @escaping (Error?) -> Void
 182 |   ) {
 183 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 184 |     configuration.activates = true
 185 |     NSWorkspace.shared.open(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:206:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 204 | 
 205 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 206 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 207 |     configuration.activates = true
 208 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:561:14: warning: no 'async' operations occur within 'await' expression
 559 |     }.store(in: &subscriptions)
 560 |     let itemsSubscription = library.$items.sink { [weak self] _ in
 561 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 562 |     }
 563 |     let signalsSubscription = library.$signals.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:564:14: warning: no 'async' operations occur within 'await' expression
 562 |     }
 563 |     let signalsSubscription = library.$signals.sink { [weak self] _ in
 564 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 565 |     }
 566 |     itemsSubscription.store(in: &subscriptions)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:569:14: warning: no 'async' operations occur within 'await' expression
 567 |     signalsSubscription.store(in: &subscriptions)
 568 |     library.$todayRefreshGeneration.sink { [weak self] _ in
 569 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 570 |     }.store(in: &subscriptions)
 571 |     library.$scanState.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:572:14: warning: no 'async' operations occur within 'await' expression
 570 |     }.store(in: &subscriptions)
 571 |     library.$scanState.sink { [weak self] _ in
 572 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 573 |     }.store(in: &subscriptions)
 574 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:575:14: warning: no 'async' operations occur within 'await' expression
 573 |     }.store(in: &subscriptions)
 574 |     library.$refreshState.sink { [weak self] _ in
 575 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 576 |     }.store(in: &subscriptions)
 577 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2732:7: warning: result of call to 'openSelected' is unused [#no-usage]
2730 |       openWithDefaultApp(item)
2731 |     case .note, .reveal:
2732 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2733 |     }
2734 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2764:9: warning: no 'async' operations occur within 'await' expression
2762 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
2763 |       Task {
2764 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
2765 |       }
2766 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2791:9: warning: no 'async' operations occur within 'await' expression
2789 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
2790 |       Task {
2791 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
2792 |       }
2793 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2849:9: warning: no 'async' operations occur within 'await' expression
2847 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
2848 |       Task {
2849 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
2850 |           itemID: item.id,
2851 |           title: item.title.text,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2880:9: warning: no 'async' operations occur within 'await' expression
2878 |     opener.openWithDefaultApp(pdf) { [weak self] error in
2879 |       Task {
2880 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
2881 |           itemID: item.id,
2882 |           title: item.title.text,
[141/179] Compiling BobMacCapture RefsPanelView.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:519:21: warning: expression of type 'Bool' is unused [#no-usage]
517 |   private func refreshSnapshotAfterRename() async {
518 |     while let current = snapshotTask {
519 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
520 |     }
521 |     refreshSnapshot(reason: .manual)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:523:21: warning: expression of type 'Bool' is unused [#no-usage]
521 |     refreshSnapshot(reason: .manual)
522 |     while let current = snapshotTask {
523 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
524 |     }
525 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:780:21: warning: expression of type 'Bool' is unused [#no-usage]
778 |   private func runPostScanRefresh() async {
779 |     while let current = snapshotTask {
780 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
781 |       if snapshotTask == nil {
782 |         break

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:787:21: warning: expression of type 'Bool' is unused [#no-usage]
785 |     refresh(reason: .scan)
786 |     while let current = snapshotTask {
787 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
788 |       if snapshotTask == nil {
789 |         break

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:851:16: warning: no 'async' operations occur within 'await' expression
849 |           return
850 |         }
851 |         Task { await self?.handleWatcherChange() }
    |                `- warning: no 'async' operations occur within 'await' expression
852 |       },
853 |       onFailure: { [weak self] message in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:854:16: warning: no 'async' operations occur within 'await' expression
852 |       },
853 |       onFailure: { [weak self] message in
854 |         Task { await self?.watcherFailed(message) }
    |                `- warning: no 'async' operations occur within 'await' expression
855 |       }
856 |     )

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsListView.swift:213:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
211 |         // rows report nil, which never clears the current rect.
212 |         .onGeometryChange(for: CGRect?.self) { proxy in
213 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
214 |             ? proxy.frame(in: .named("refsPanel")) : nil
215 |         } action: { rect in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:38: note: property declared here
 287 |     return tabsFilter && tabsListing?.tabs[id] != nil
 288 |   }
 289 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 290 |     didSet {
 291 |       if oldValue != selectedID {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsListView.swift:251:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
249 |       .transition(removalTransition)
250 |       .onGeometryChange(for: CGRect?.self) { proxy in
251 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
252 |           ? proxy.frame(in: .named("refsPanel")) : nil
253 |       } action: { rect in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:38: note: property declared here
 287 |     return tabsFilter && tabsListing?.tabs[id] != nil
 288 |   }
 289 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 290 |     didSet {
 291 |       if oldValue != selectedID {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:183:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 181 |     completion: @escaping (Error?) -> Void
 182 |   ) {
 183 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 184 |     configuration.activates = true
 185 |     NSWorkspace.shared.open(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:206:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 204 | 
 205 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 206 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 207 |     configuration.activates = true
 208 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:561:14: warning: no 'async' operations occur within 'await' expression
 559 |     }.store(in: &subscriptions)
 560 |     let itemsSubscription = library.$items.sink { [weak self] _ in
 561 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 562 |     }
 563 |     let signalsSubscription = library.$signals.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:564:14: warning: no 'async' operations occur within 'await' expression
 562 |     }
 563 |     let signalsSubscription = library.$signals.sink { [weak self] _ in
 564 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 565 |     }
 566 |     itemsSubscription.store(in: &subscriptions)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:569:14: warning: no 'async' operations occur within 'await' expression
 567 |     signalsSubscription.store(in: &subscriptions)
 568 |     library.$todayRefreshGeneration.sink { [weak self] _ in
 569 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 570 |     }.store(in: &subscriptions)
 571 |     library.$scanState.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:572:14: warning: no 'async' operations occur within 'await' expression
 570 |     }.store(in: &subscriptions)
 571 |     library.$scanState.sink { [weak self] _ in
 572 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 573 |     }.store(in: &subscriptions)
 574 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:575:14: warning: no 'async' operations occur within 'await' expression
 573 |     }.store(in: &subscriptions)
 574 |     library.$refreshState.sink { [weak self] _ in
 575 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 576 |     }.store(in: &subscriptions)
 577 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2732:7: warning: result of call to 'openSelected' is unused [#no-usage]
2730 |       openWithDefaultApp(item)
2731 |     case .note, .reveal:
2732 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2733 |     }
2734 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2764:9: warning: no 'async' operations occur within 'await' expression
2762 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
2763 |       Task {
2764 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
2765 |       }
2766 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2791:9: warning: no 'async' operations occur within 'await' expression
2789 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
2790 |       Task {
2791 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
2792 |       }
2793 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2849:9: warning: no 'async' operations occur within 'await' expression
2847 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
2848 |       Task {
2849 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
2850 |           itemID: item.id,
2851 |           title: item.title.text,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2880:9: warning: no 'async' operations occur within 'await' expression
2878 |     opener.openWithDefaultApp(pdf) { [weak self] error in
2879 |       Task {
2880 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
2881 |           itemID: item.id,
2882 |           title: item.title.text,
[142/179] Compiling BobMacCapture RefsQuoteText.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:519:21: warning: expression of type 'Bool' is unused [#no-usage]
517 |   private func refreshSnapshotAfterRename() async {
518 |     while let current = snapshotTask {
519 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
520 |     }
521 |     refreshSnapshot(reason: .manual)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:523:21: warning: expression of type 'Bool' is unused [#no-usage]
521 |     refreshSnapshot(reason: .manual)
522 |     while let current = snapshotTask {
523 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
524 |     }
525 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:780:21: warning: expression of type 'Bool' is unused [#no-usage]
778 |   private func runPostScanRefresh() async {
779 |     while let current = snapshotTask {
780 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
781 |       if snapshotTask == nil {
782 |         break

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:787:21: warning: expression of type 'Bool' is unused [#no-usage]
785 |     refresh(reason: .scan)
786 |     while let current = snapshotTask {
787 |       await current.value
    |                     `- warning: expression of type 'Bool' is unused [#no-usage]
788 |       if snapshotTask == nil {
789 |         break

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:851:16: warning: no 'async' operations occur within 'await' expression
849 |           return
850 |         }
851 |         Task { await self?.handleWatcherChange() }
    |                `- warning: no 'async' operations occur within 'await' expression
852 |       },
853 |       onFailure: { [weak self] message in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsLibrary.swift:854:16: warning: no 'async' operations occur within 'await' expression
852 |       },
853 |       onFailure: { [weak self] message in
854 |         Task { await self?.watcherFailed(message) }
    |                `- warning: no 'async' operations occur within 'await' expression
855 |       }
856 |     )

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsListView.swift:213:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
211 |         // rows report nil, which never clears the current rect.
212 |         .onGeometryChange(for: CGRect?.self) { proxy in
213 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
214 |             ? proxy.frame(in: .named("refsPanel")) : nil
215 |         } action: { rect in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:38: note: property declared here
 287 |     return tabsFilter && tabsListing?.tabs[id] != nil
 288 |   }
 289 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 290 |     didSet {
 291 |       if oldValue != selectedID {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsListView.swift:251:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
249 |       .transition(removalTransition)
250 |       .onGeometryChange(for: CGRect?.self) { proxy in
251 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
252 |           ? proxy.frame(in: .named("refsPanel")) : nil
253 |       } action: { rect in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:289:38: note: property declared here
 287 |     return tabsFilter && tabsListing?.tabs[id] != nil
 288 |   }
 289 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 290 |     didSet {
 291 |       if oldValue != selectedID {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:183:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 181 |     completion: @escaping (Error?) -> Void
 182 |   ) {
 183 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 184 |     configuration.activates = true
 185 |     NSWorkspace.shared.open(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:206:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 204 | 
 205 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 206 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 207 |     configuration.activates = true
 208 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:561:14: warning: no 'async' operations occur within 'await' expression
 559 |     }.store(in: &subscriptions)
 560 |     let itemsSubscription = library.$items.sink { [weak self] _ in
 561 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 562 |     }
 563 |     let signalsSubscription = library.$signals.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:564:14: warning: no 'async' operations occur within 'await' expression
 562 |     }
 563 |     let signalsSubscription = library.$signals.sink { [weak self] _ in
 564 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 565 |     }
 566 |     itemsSubscription.store(in: &subscriptions)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:569:14: warning: no 'async' operations occur within 'await' expression
 567 |     signalsSubscription.store(in: &subscriptions)
 568 |     library.$todayRefreshGeneration.sink { [weak self] _ in
 569 |       Task { await self?.libraryDidPublish() }
     |              `- warning: no 'async' operations occur within 'await' expression
 570 |     }.store(in: &subscriptions)
 571 |     library.$scanState.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:572:14: warning: no 'async' operations occur within 'await' expression
 570 |     }.store(in: &subscriptions)
 571 |     library.$scanState.sink { [weak self] _ in
 572 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 573 |     }.store(in: &subscriptions)
 574 |     library.$refreshState.sink { [weak self] _ in

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:575:14: warning: no 'async' operations occur within 'await' expression
 573 |     }.store(in: &subscriptions)
 574 |     library.$refreshState.sink { [weak self] _ in
 575 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 576 |     }.store(in: &subscriptions)
 577 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2732:7: warning: result of call to 'openSelected' is unused [#no-usage]
2730 |       openWithDefaultApp(item)
2731 |     case .note, .reveal:
2732 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
2733 |     }
2734 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2764:9: warning: no 'async' operations occur within 'await' expression
2762 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
2763 |       Task {
2764 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
2765 |       }
2766 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2791:9: warning: no 'async' operations occur within 'await' expression
2789 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
2790 |       Task {
2791 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
2792 |       }
2793 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2849:9: warning: no 'async' operations occur within 'await' expression
2847 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
2848 |       Task {
2849 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
2850 |           itemID: item.id,
2851 |           title: item.title.text,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/Refs/RefsPanelModel.swift:2880:9: warning: no 'async' operations occur within 'await' expression
2878 |     opener.openWithDefaultApp(pdf) { [weak self] error in
2879 |       Task {
2880 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
2881 |           itemID: item.id,
2882 |           title: item.title.text,
[143/179] Compiling BobMacCapture AccessibilityTrust.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
824 |     }
825 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
824 |     }
825 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:76:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |     NSApplication.shared.addSceneRepresentation(representation)
 75 |     settingsSceneRepresentation = representation
 76 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |       representation.environment.openSettings()
 78 |     }
    :
818 |   var activateApplication: () -> Void
819 | 
820 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:271:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
269 |     menu.addItem(redo)
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
273 |     menu.addItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:272:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
273 |     menu.addItem(
274 |       NSMenuItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:281:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     )
280 |     menu.addItem(
281 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     return menu
283 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:475:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |   /// off MainActor state.
474 |   nonisolated static func storedHighlightsAppPath() -> String {
475 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
476 |   }
477 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:555:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
553 |       library: library,
554 |       opener: WorkspaceRefsOpener(),
555 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
556 |       tabs: tabsSession,
557 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:730:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
728 |       return
729 |     }
730 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
731 |   }
732 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[144/179] Compiling BobMacCapture AppDelegate.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
824 |     }
825 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
824 |     }
825 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:76:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |     NSApplication.shared.addSceneRepresentation(representation)
 75 |     settingsSceneRepresentation = representation
 76 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |       representation.environment.openSettings()
 78 |     }
    :
818 |   var activateApplication: () -> Void
819 | 
820 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:271:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
269 |     menu.addItem(redo)
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
273 |     menu.addItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:272:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
273 |     menu.addItem(
274 |       NSMenuItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:281:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     )
280 |     menu.addItem(
281 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     return menu
283 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:475:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |   /// off MainActor state.
474 |   nonisolated static func storedHighlightsAppPath() -> String {
475 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
476 |   }
477 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:555:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
553 |       library: library,
554 |       opener: WorkspaceRefsOpener(),
555 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
556 |       tabs: tabsSession,
557 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:730:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
728 |       return
729 |     }
730 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
731 |   }
732 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[145/179] Compiling BobMacCapture AppRelauncher.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
824 |     }
825 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
824 |     }
825 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:76:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |     NSApplication.shared.addSceneRepresentation(representation)
 75 |     settingsSceneRepresentation = representation
 76 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |       representation.environment.openSettings()
 78 |     }
    :
818 |   var activateApplication: () -> Void
819 | 
820 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:271:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
269 |     menu.addItem(redo)
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
273 |     menu.addItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:272:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
273 |     menu.addItem(
274 |       NSMenuItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:281:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     )
280 |     menu.addItem(
281 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     return menu
283 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:475:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |   /// off MainActor state.
474 |   nonisolated static func storedHighlightsAppPath() -> String {
475 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
476 |   }
477 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:555:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
553 |       library: library,
554 |       opener: WorkspaceRefsOpener(),
555 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
556 |       tabs: tabsSession,
557 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:730:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
728 |       return
729 |     }
730 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
731 |   }
732 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[146/179] Compiling BobMacCapture AppSettings.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
824 |     }
825 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
824 |     }
825 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:76:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |     NSApplication.shared.addSceneRepresentation(representation)
 75 |     settingsSceneRepresentation = representation
 76 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |       representation.environment.openSettings()
 78 |     }
    :
818 |   var activateApplication: () -> Void
819 | 
820 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:271:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
269 |     menu.addItem(redo)
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
273 |     menu.addItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:272:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
273 |     menu.addItem(
274 |       NSMenuItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:281:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     )
280 |     menu.addItem(
281 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     return menu
283 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:475:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |   /// off MainActor state.
474 |   nonisolated static func storedHighlightsAppPath() -> String {
475 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
476 |   }
477 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:555:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
553 |       library: library,
554 |       opener: WorkspaceRefsOpener(),
555 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
556 |       tabs: tabsSession,
557 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:730:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
728 |       return
729 |     }
730 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
731 |   }
732 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[147/179] Compiling BobMacCapture BlockDiffCard.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
824 |     }
825 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
824 |     }
825 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:76:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |     NSApplication.shared.addSceneRepresentation(representation)
 75 |     settingsSceneRepresentation = representation
 76 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |       representation.environment.openSettings()
 78 |     }
    :
818 |   var activateApplication: () -> Void
819 | 
820 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:271:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
269 |     menu.addItem(redo)
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
273 |     menu.addItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:272:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
273 |     menu.addItem(
274 |       NSMenuItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:281:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     )
280 |     menu.addItem(
281 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     return menu
283 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:475:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |   /// off MainActor state.
474 |   nonisolated static func storedHighlightsAppPath() -> String {
475 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
476 |   }
477 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:555:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
553 |       library: library,
554 |       opener: WorkspaceRefsOpener(),
555 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
556 |       tabs: tabsSession,
557 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:730:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
728 |       return
729 |     }
730 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
731 |   }
732 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[148/179] Compiling BobMacCapture BlockIDField.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
824 |     }
825 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
824 |     }
825 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:76:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |     NSApplication.shared.addSceneRepresentation(representation)
 75 |     settingsSceneRepresentation = representation
 76 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |       representation.environment.openSettings()
 78 |     }
    :
818 |   var activateApplication: () -> Void
819 | 
820 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:271:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
269 |     menu.addItem(redo)
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
273 |     menu.addItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:272:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
273 |     menu.addItem(
274 |       NSMenuItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:281:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     )
280 |     menu.addItem(
281 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     return menu
283 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:475:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |   /// off MainActor state.
474 |   nonisolated static func storedHighlightsAppPath() -> String {
475 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
476 |   }
477 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:555:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
553 |       library: library,
554 |       opener: WorkspaceRefsOpener(),
555 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
556 |       tabs: tabsSession,
557 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:730:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
728 |       return
729 |     }
730 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
731 |   }
732 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[149/179] Compiling BobMacCapture BobMacCaptureMain.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
824 |     }
825 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
824 |     }
825 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:76:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |     NSApplication.shared.addSceneRepresentation(representation)
 75 |     settingsSceneRepresentation = representation
 76 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |       representation.environment.openSettings()
 78 |     }
    :
818 |   var activateApplication: () -> Void
819 | 
820 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:271:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
269 |     menu.addItem(redo)
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
273 |     menu.addItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:272:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
273 |     menu.addItem(
274 |       NSMenuItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:281:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     )
280 |     menu.addItem(
281 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     return menu
283 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:475:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |   /// off MainActor state.
474 |   nonisolated static func storedHighlightsAppPath() -> String {
475 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
476 |   }
477 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:555:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
553 |       library: library,
554 |       opener: WorkspaceRefsOpener(),
555 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
556 |       tabs: tabsSession,
557 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:730:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
728 |       return
729 |     }
730 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
731 |   }
732 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[150/179] Compiling BobMacCapture BobPanelCoordinator.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
824 |     }
825 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
824 |     }
825 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:76:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |     NSApplication.shared.addSceneRepresentation(representation)
 75 |     settingsSceneRepresentation = representation
 76 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |       representation.environment.openSettings()
 78 |     }
    :
818 |   var activateApplication: () -> Void
819 | 
820 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:271:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
269 |     menu.addItem(redo)
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
273 |     menu.addItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:272:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
273 |     menu.addItem(
274 |       NSMenuItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:281:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     )
280 |     menu.addItem(
281 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     return menu
283 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:475:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |   /// off MainActor state.
474 |   nonisolated static func storedHighlightsAppPath() -> String {
475 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
476 |   }
477 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:555:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
553 |       library: library,
554 |       opener: WorkspaceRefsOpener(),
555 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
556 |       tabs: tabsSession,
557 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:730:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
728 |       return
729 |     }
730 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
731 |   }
732 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[151/179] Compiling BobMacCapture BundleSigningInspector.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                            `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
824 |     }
825 |   ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:823:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {
823 |       NSApplication.shared.activate()
    |                     `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
824 |     }
825 |   ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:76:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 74 |     NSApplication.shared.addSceneRepresentation(representation)
 75 |     settingsSceneRepresentation = representation
 76 |     settingsPresentation = SettingsPresentation {
    |                                                 `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
 77 |       representation.environment.openSettings()
 78 |     }
    :
818 |   var activateApplication: () -> Void
819 | 
820 |   init(
    |   `- note: 'init(openSettings:activateApplication:)' declared here
821 |     openSettings: @escaping () -> Void = {},
822 |     activateApplication: @escaping () -> Void = {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:271:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
269 |     menu.addItem(redo)
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
273 |     menu.addItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:272:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
270 |     menu.addItem(.separator())
271 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
272 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
273 |     menu.addItem(
274 |       NSMenuItem(

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:281:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
279 |     )
280 |     menu.addItem(
281 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
282 |     return menu
283 |   }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:475:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
473 |   /// off MainActor state.
474 |   nonisolated static func storedHighlightsAppPath() -> String {
475 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
476 |   }
477 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:555:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
553 |       library: library,
554 |       opener: WorkspaceRefsOpener(),
555 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
556 |       tabs: tabsSession,
557 |       isAdHocSigned: { signingState == .adHoc }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppDelegate.swift:730:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
728 |       return
729 |     }
730 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
731 |   }
732 | 

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/AppSettings.swift:188:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[152/179] Compiling BobMacCapture CanceledDraftStash.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[153/179] Compiling BobMacCapture CaptureAgendaRowMeasurer.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[154/179] Compiling BobMacCapture CaptureAgendaStore.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[155/179] Compiling BobMacCapture CaptureAgendaView.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[156/179] Compiling BobMacCapture CaptureEditorPalette.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[157/179] Compiling BobMacCapture CaptureEditorTextConfiguration.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[158/179] Compiling BobMacCapture CaptureKeyCommandRouter.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[159/179] Compiling BobMacCapture CapturePanelController.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[160/179] Compiling BobMacCapture CapturePanelModel.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:365:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
363 |                 Task { [weak self] in
364 |                     await MainActor.run {
365 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
366 |                     }
367 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:378:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
376 |                 Task { [weak self] in
377 |                     await MainActor.run {
378 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
379 |                     }
380 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:391:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
389 |                 Task { [weak self] in
390 |                     await MainActor.run {
391 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
392 |                     }
393 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaStore.swift:404:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
402 |                 Task { [weak self] in
403 |                     await MainActor.run {
404 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
405 |                     }
406 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelController.swift:1405:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1403 |         }
1404 | 
1405 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1406 |         return true
1407 |     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:1802:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1800 |                         refuseOverride: !allowsOverride,
1801 |                         pullInCapabilityAdvertised: capabilityAdvertised,
1802 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
     |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
1803 |                     )
1804 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7314:23: warning: no 'async' operations occur within 'await' expression
7312 |                 }
7313 | 
7314 |                 guard await self?.isCurrentAnalysis(generation) == true else {
     |                       `- warning: no 'async' operations occur within 'await' expression
7315 |                     return
7316 |                 }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7319:21: warning: no 'async' operations occur within 'await' expression
7317 | 
7318 |                 if pickerNeeded == nil {
7319 |                     await self?.startLivePreview(
     |                     `- warning: no 'async' operations occur within 'await' expression
7320 |                         draft: draft,
7321 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7333:27: warning: no 'async' operations occur within 'await' expression
7331 |                     await completionGate.value
7332 |                     try Task.checkCancellation()
7333 |                     guard await self?.isCurrentAnalysis(generation) == true else {
     |                           `- warning: no 'async' operations occur within 'await' expression
7334 |                         return
7335 |                     }

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7340:20: warning: no 'async' operations occur within 'await' expression
7338 |                 if let cursorUTF8Offset,
7339 |                    requestCompletion,
7340 |                    await self?.shouldRequestCompletion(
     |                    `- warning: no 'async' operations occur within 'await' expression
7341 |                        parse: parse,
7342 |                        cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7346:37: warning: no 'async' operations occur within 'await' expression
7344 |                    ) == true
7345 |                 {
7346 |                     if let cached = await self?.cachedRouteCompletion(
     |                                     `- warning: no 'async' operations occur within 'await' expression
7347 |                         parse: parse,
7348 |                         cursor: cursorUTF8Offset,

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePanelModel.swift:7562:28: warning: no 'async' operations occur within 'await' expression
7560 |         Task { [weak self, processClient] in
7561 |             do {
7562 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
     |                            `- warning: no 'async' operations occur within 'await' expression
7563 |                 let processClientIdentity = processClient.identityToken
7564 |                 let preview = try await CaptureSignpost.measure("preview") {

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[161/179] Compiling BobMacCapture CapturePanelView.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[162/179] Compiling BobMacCapture CapturePanelWindowSizer.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[163/179] Compiling BobMacCapture CapturePickerFilterField.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[164/179] Compiling BobMacCapture CapturePickerState.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[165/179] Compiling BobMacCapture CapturePickerView.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[166/179] Compiling BobMacCapture CapturePlanBudgetMeterRow.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[167/179] Compiling BobMacCapture CapturePullInChoice.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[168/179] Compiling BobMacCapture CapturePullInChoiceView.swift
/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bobmac-bigpanel.fix1/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[169/179] Compiling BobMacCapture RefsRenameCardView.swift
[170/179] Compiling BobMacCapture RefsRowView.swift
[171/179] Compiling BobMacCapture RefsSearchBar.swift
[172/179] Compiling BobMacCapture RefsTabsViews.swift
[173/179] Compiling BobMacCapture RefsTodayLinkCardView.swift
[174/179] Compiling BobMacCapture RefsVisualTokens.swift
[175/179] Compiling BobMacCapture RefsHighlightsOpenKey.swift
[176/179] Compiling BobMacCapture RefsHighlightsTabsKey.swift
[176/179] Write Objects.LinkFileList
[177/179] Linking BobMacCapture
[178/179] Applying BobMacCapture
Build complete! (77.19s)
PASS BobMacCaptureTests
PASS BobMacCaptureInstallHelperTests
PASS CaptureCoreTests
PASS RefsCoreTests
Type-check only: macOS test targets were checked against a stub; CI still runs the tests.
X11 forwarding request failed on channel 0
OLD_SCRATCH_REMOVED
succeeded  exit=0  duration=248346ms

