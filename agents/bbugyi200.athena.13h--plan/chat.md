# Chat History - ace-run (13h--plan)

- **TIMESTAMP:** 2026-10-23 16:40:37 EDT
- **MODEL:** claude/opus
- **AGENT:** 13h--plan

## Linked Chats

- **1. --plan** — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-13h__plan-261023_163005.md`
- 2. --code — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-13h__code-261023_163005.md`

**Plan:** /home/bryan/.sase/plans/202610/fix_mac_capture_scan_receipt_build.md


## Prompt

#gh:gh_bobs-org__bob-cli The bob-mac-capture app is no longer building (see the command output below for
context). Can you help me diagnose the root cause of this issue and fix it? Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.

%m:@xlarge %auto
```
  $ just --justfile ~/projects/github/bobs-org/bob-mac-capture/justfile install ~/Applications
./Scripts/install.sh --target "/Users/bbugyi/Applications" --identity ""
[1/1] Planning build
Building for production...
/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 |
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 |
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 |
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 |
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 |
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 |
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/CaptureModels.swift:6090:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6088 | }
6089 |
6090 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
6091 |   public let replacement: String
6092 |   public let route: String?
/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/RefsCore/RefsRename.swift:17:8: warning: no calls to throwing functions occur within 'try' expression
 15 |   public init(from decoder: Decoder) throws {
 16 |     let container = try decoder.singleValueContainer()
 17 |     if try container.decodeNil() {
    |        `- warning: no calls to throwing functions occur within 'try' expression
 18 |       self = .null
 19 |     } else if let value = try? container.decode(Bool.self) {

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/RefsCore/RefsStores.swift:43:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/RefsCore/RefsStores.swift:184:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/RefsCore/RefsStores.swift:378:15: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppDelegate.swift:902:28: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppDelegate.swift:902:21: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppDelegate.swift:81:49: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CaptureAgendaStore.swift:77:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 75 |         processClient: BobProcessClient? = nil,
 76 |         vaultRootPath: String = "",
 77 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         now: @Sendable @escaping () -> Date = { Date() },
 79 |         workspaceCenter: NotificationCenter? = nil,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppDelegate.swift:285:51: warning: use '#selector' instead of explicitly constructing a 'Selector'
283 |     menu.addItem(redo)
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
    |                                                   `- warning: use '#selector' instead of explicitly constructing a 'Selector'
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
287 |     menu.addItem(

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppDelegate.swift:286:52: warning: use '#selector' instead of explicitly constructing a 'Selector'
284 |     menu.addItem(.separator())
285 |     menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
286 |     menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
    |                                                    `- warning: use '#selector' instead of explicitly constructing a 'Selector'
287 |     menu.addItem(
288 |       NSMenuItem(

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppDelegate.swift:295:47: warning: use '#selector' instead of explicitly constructing a 'Selector'
293 |     )
294 |     menu.addItem(
295 |       NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
    |                                               `- warning: use '#selector' instead of explicitly constructing a 'Selector'
296 |     return menu
297 |   }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppDelegate.swift:492:54: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
490 |   /// off MainActor state.
491 |   nonisolated static func storedHighlightsAppPath() -> String {
492 |     UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
    |                                                      `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
493 |   }
494 |

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 |
 11 |     @Published var bobExecutableOverride: String {

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppDelegate.swift:572:56: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
570 |       library: library,
571 |       opener: WorkspaceRefsOpener(),
572 |       highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
    |                                                        `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
573 |       tabs: tabsSession,
574 |       isAdHocSigned: { signingState == .adHoc }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsScanReceiptObserver.swift:29:74: warning: converting function value of type '@MainActor (@escaping @Sendable () -> Void) -> Int32?' to '(@escaping @Sendable () -> Void) -> Int32?' loses global actor 'MainActor'; this is an error in the Swift 6 language mode
 27 |     init(
 28 |         reader: RefsScanReceiptReader = RefsScanReceiptReader(),
 29 |         register: @escaping (@escaping @Sendable () -> Void) -> Int32? = Self.registerLive,
    |                                                                          `- warning: converting function value of type '@MainActor (@escaping @Sendable () -> Void) -> Int32?' to '(@escaping @Sendable () -> Void) -> Int32?' loses global actor 'MainActor'; this is an error in the Swift 6 language mode
 30 |         cancel: @escaping (Int32) -> Void = { token in _ = notify_cancel(token) }
 31 |     ) {

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsScanReceiptObserver.swift:30:60: error: cannot find 'notify_cancel' in scope
 28 |         reader: RefsScanReceiptReader = RefsScanReceiptReader(),
 29 |         register: @escaping (@escaping @Sendable () -> Void) -> Int32? = Self.registerLive,
 30 |         cancel: @escaping (Int32) -> Void = { token in _ = notify_cancel(token) }
    |                                                            `- error: cannot find 'notify_cancel' in scope
 31 |     ) {
 32 |         self.reader = reader

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppDelegate.swift:808:22: warning: use '#selector' instead of explicitly constructing a 'Selector'
806 |       return
807 |     }
808 |     NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
    |                      `- warning: use '#selector' instead of explicitly constructing a 'Selector'
809 |   }
810 |

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/AppSettings.swift:204:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CaptureAgendaStore.swift:367:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
365 |                 Task { [weak self] in
366 |                     await MainActor.run {
367 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                     }
369 |                 }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CaptureAgendaStore.swift:380:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
378 |                 Task { [weak self] in
379 |                     await MainActor.run {
380 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                     }
382 |                 }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CaptureAgendaStore.swift:393:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
391 |                 Task { [weak self] in
392 |                     await MainActor.run {
393 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                     }
395 |                 }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CaptureAgendaStore.swift:406:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
404 |                 Task { [weak self] in
405 |                     await MainActor.run {
406 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                     }
408 |                 }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CaptureAgendaView.swift:1064:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1062 |         for segment in parsed.segments {
1063 |             let slice = String(chars[segment.range])
1064 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1065 |         }
1066 |         return result.font(base).foregroundStyle(color)

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelController.swift:1430:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1428 |         }
1429 |
1430 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1431 |         return true
1432 |     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelController.swift:1997:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1995 |         }
1996 |         if let textView = firstResponder as? NSTextView,
1997 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
1998 |            field.accessibilityIdentifier() == identifier
1999 |         {

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:2028:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2026 |                         refuseOverride: !allowsOverride,
 2027 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2028 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2029 |                     )
 2030 |                 }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:2028:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2026 |                         refuseOverride: !allowsOverride,
 2027 |                         pullInCapabilityAdvertised: capabilityAdvertised,
 2028 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2029 |                     )
 2030 |                 }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:8680:23: warning: no 'async' operations occur within 'await' expression
 8678 |                 }
 8679 |
 8680 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
 8681 |                     return
 8682 |                 }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:8685:21: warning: no 'async' operations occur within 'await' expression
 8683 |
 8684 |                 if pickerNeeded == nil {
 8685 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
 8686 |                         draft: draft,
 8687 |                         previewDraft: closePending?.trimmed ?? draft,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:8699:27: warning: no 'async' operations occur within 'await' expression
 8697 |                     await completionGate.value
 8698 |                     try Task.checkCancellation()
 8699 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
 8700 |                         return
 8701 |                     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:8706:20: warning: no 'async' operations occur within 'await' expression
 8704 |                 if let cursorUTF8Offset,
 8705 |                    requestCompletion,
 8706 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
 8707 |                        parse: parse,
 8708 |                        cursor: cursorUTF8Offset,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:8712:37: warning: no 'async' operations occur within 'await' expression
 8710 |                    ) == true
 8711 |                 {
 8712 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
 8713 |                         parse: parse,
 8714 |                         cursor: cursorUTF8Offset,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift:8941:28: warning: no 'async' operations occur within 'await' expression
 8939 |         Task { [weak self, processClient] in
 8940 |             do {
 8941 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
 8942 |                 let processClientIdentity = processClient.identityToken
 8943 |                 let preview = try await CaptureSignpost.measure("preview") {

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

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 |
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsLibrary.swift:157:21: note: static property declared here
 155 |
 156 |   /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 157 |   public static let pullThrottleInterval: TimeInterval = 5
     |                     `- note: static property declared here
 158 |
 159 |   private var fetcher: RefsFetching?

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 |
11 |     /// Returns true when the refresh should run, recording the start.

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:32: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 |

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsLibrary.swift:606:21: warning: expression of type 'Bool' is unused [#no-usage]
 604 |   private func refreshSnapshotAfterRename() async {
 605 |     while let current = snapshotTask {
 606 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 607 |     }
 608 |     refreshSnapshot(reason: .manual)

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsLibrary.swift:610:21: warning: expression of type 'Bool' is unused [#no-usage]
 608 |     refreshSnapshot(reason: .manual)
 609 |     while let current = snapshotTask {
 610 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 611 |     }
 612 |   }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsLibrary.swift:873:21: warning: expression of type 'Bool' is unused [#no-usage]
 871 |   private func runPostScanRefresh() async {
 872 |     while let current = snapshotTask {
 873 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 874 |       if snapshotTask == nil {
 875 |         break

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsLibrary.swift:880:21: warning: expression of type 'Bool' is unused [#no-usage]
 878 |     refresh(reason: .scan)
 879 |     while let current = snapshotTask {
 880 |       await current.value
     |                     `- warning: expression of type 'Bool' is unused [#no-usage]
 881 |       if snapshotTask == nil {
 882 |         break

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsLibrary.swift:944:16: warning: no 'async' operations occur within 'await' expression
 942 |           return
 943 |         }
 944 |         Task { await self?.handleWatcherChange() }
     |                `- warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsLibrary.swift:947:16: warning: no 'async' operations occur within 'await' expression
 945 |       },
 946 |       onFailure: { [weak self] message in
 947 |         Task { await self?.watcherFailed(message) }
     |                `- warning: no 'async' operations occur within 'await' expression
 948 |       }
 949 |     )

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsListView.swift:271:17: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
269 |         // rows report nil, which never clears the current rect.
270 |         .onGeometryChange(for: CGRect?.self) { proxy in
271 |           model.selectedID == id
    |                 `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
272 |             ? proxy.frame(in: .named("refsPanel")) : nil
273 |         } action: { rect in

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsListView.swift:319:15: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
317 |       .transition(removalTransition)
318 |       .onGeometryChange(for: CGRect?.self) { proxy in
319 |         model.selectedID == id
    |               `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
320 |           ? proxy.frame(in: .named("refsPanel")) : nil
321 |       } action: { rect in

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:316:38: note: property declared here
 314 |     return tabsFilter && tabsListing?.tabs[id] != nil
 315 |   }
 316 |   @Published public private(set) var selectedID: String? {
     |                                      `- note: property declared here
 317 |     didSet {
 318 |       if panelIsVisible(), let selectedID {

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:193:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 191 |     completion: @escaping (Error?) -> Void
 192 |   ) {
 193 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 194 |     configuration.activates = true
 195 |     NSWorkspace.shared.open(

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:216:9: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 214 |
 215 |   public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 216 |     var configuration = NSWorkspace.OpenConfiguration()
     |         `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 217 |     configuration.activates = true
 218 |     NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:632:14: warning: no 'async' operations occur within 'await' expression
 630 |     }.store(in: &subscriptions)
 631 |     library.$scanState.sink { [weak self] _ in
 632 |       Task { await self?.scanStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:635:14: warning: no 'async' operations occur within 'await' expression
 633 |     }.store(in: &subscriptions)
 634 |     library.$refreshState.sink { [weak self] _ in
 635 |       Task { await self?.refreshStateDidChange() }
     |              `- warning: no 'async' operations occur within 'await' expression
 636 |     }.store(in: &subscriptions)
 637 |   }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3050:7: warning: result of call to 'openSelected' is unused [#no-usage]
3048 |       openWithDefaultApp(item)
3049 |     case .note, .reveal:
3050 |       openSelected(pending.target)
     |       `- warning: result of call to 'openSelected' is unused [#no-usage]
3051 |     }
3052 |   }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3082:9: warning: no 'async' operations occur within 'await' expression
3080 |     opener.openInHighlights(closed.url, app: app) { [weak self] error in
3081 |       Task {
3082 |         await self?.finishClosedTabOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3083 |       }
3084 |     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3109:9: warning: no 'async' operations occur within 'await' expression
3107 |     opener.openWithDefaultApp(closed.url) { [weak self] error in
3108 |       Task {
3109 |         await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |         `- warning: no 'async' operations occur within 'await' expression
3110 |       }
3111 |     }

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3167:9: warning: no 'async' operations occur within 'await' expression
3165 |     opener.openInHighlights(pdf, app: app) { [weak self] error in
3166 |       Task {
3167 |         await self?.finishHighlightsOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3168 |           itemID: item.id,
3169 |           title: item.title.text,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3198:9: warning: no 'async' operations occur within 'await' expression
3196 |     opener.openWithDefaultApp(pdf) { [weak self] error in
3197 |       Task {
3198 |         await self?.finishDefaultAppOpen(
     |         `- warning: no 'async' operations occur within 'await' expression
3199 |           itemID: item.id,
3200 |           title: item.title.text,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsScanReceiptObserver.swift:29:74: error: covariant 'Self' type cannot be referenced from a default argument expression
 27 |     init(
 28 |         reader: RefsScanReceiptReader = RefsScanReceiptReader(),
 29 |         register: @escaping (@escaping @Sendable () -> Void) -> Int32? = Self.registerLive,
    |                                                                          `- error: covariant 'Self' type cannot be referenced from a default argument expression
 30 |         cancel: @escaping (Int32) -> Void = { token in _ = notify_cancel(token) }
 31 |     ) {

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/Refs/RefsScanReceiptObserver.swift:101:22: error: cannot find 'notify_register_dispatch' in scope
 99 |     private static func registerLive(_ handler: @escaping @Sendable () -> Void) -> Int32? {
100 |         var token: Int32 = 0
101 |         let status = notify_register_dispatch(
    |                      `- error: cannot find 'notify_register_dispatch' in scope
102 |             RefsScanReceiptReader.darwinNotificationName,
103 |             &token,

/Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
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
```

## Response

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202610/fix_mac_capture_scan_receipt_build.md`

> # Plan: Fix the Bob Mac Capture build broken by `RefsScanReceiptObserver`
> ## Goal
> Make `just install ~/Applications` (and macOS CI) build Bob Mac Capture again. All edits
> are in the linked `bob-mac-capture` repo; open it with your `/sase_repo` skill
> (`sase repo open bob-mac-capture -r "..."`) and read its `AGENTS.md` first. No bob-cli
> changes.
> ## Diagnosis (verified while planning)
> The build broke at `bob-mac-capture` commit `6dc2c12` ("feat(refs): observe scan
> receipts and notify for open PDF updates", epic phase `bob-cli-at.6`). That commit's
> macOS CI run (`40015370455`) fails in its **Build** step on exactly the three errors

*See full plan file for details.*

