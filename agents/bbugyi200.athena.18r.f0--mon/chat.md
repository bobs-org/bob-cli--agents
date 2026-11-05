# Chat History - ace-run (18r.f0--mon)

- **TIMESTAMP:** 2026-11-05 17:37:52 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** 18r.f0--mon

## Prompt

sase monitor start --command "ssh mac 'cd /tmp/bob-mac-capture-flip && ./Scripts/bundle.sh && just typecheck-tests; rc=$?; rm -rf /tmp/bob-mac-capture-flip; exit $rc'" --reason 'Type-check changed Swift on mac scratch copy (bundle plus typecheck-tests)'

## Response

sase tool run faa2435a54401f035e0cd4b913bdf8d8
X11 forwarding request failed on channel 0
Building for production...
[0/6] Write sources
[3/6] Write swift-version--1AB21518FC5DEDBE.txt
[5/7] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9431:13: warning: no calls to throwing functions occur within 'try' expression
 9429 |         let container = try decoder.singleValueContainer()
 9430 |         // Explicit null has no value; treat it as absent.
 9431 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9432 |             throw DecodingError.valueNotFound(
 9433 |                 CaptureThemeSuggestion.self,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[6/8] Compiling RefsCore HighlightsSaveScan.swift
/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {

/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 41 | 
 42 |     private let fileURL: URL
 43 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 |     private let onError: @Sendable (String) -> Void
 45 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
182 | 
183 |     private let fileURL: URL
184 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
185 |     private let onError: @Sendable (String) -> Void
186 |     private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
376 | 
377 |     private let fileURL: URL
378 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
379 |     private let onError: @Sendable (String) -> Void
380 |     private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[7/9] Compiling BobMacCapture AccessibilityTrust.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1094 |         }
1095 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1094 |         }
1095 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  81 |         NSApplication.shared.addSceneRepresentation(representation)
  82 |         settingsSceneRepresentation = representation
  83 |         settingsPresentation = SettingsPresentation {
     |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  84 |             representation.environment.openSettings()
  85 |         }
     :
1088 |     var activateApplication: () -> Void
1089 | 
1090 |     init(
     |     `- note: 'init(openSettings:activateApplication:)' declared here
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:84:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         processClient: BobProcessClient? = nil,
 83 |         vaultRootPath: String = "",
 84 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 85 |         now: @Sendable @escaping () -> Date = { Date() },
 86 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
269 |     static let refsHighlightsCodeKey = "refsHighlightsCodeKey"
270 |     static let refsHighlightsLinkKey = "refsHighlightsLinkKey"
271 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
272 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
273 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:422:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
420 |                 Task { [weak self] in
421 |                     await MainActor.run {
422 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
423 |                     }
424 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:1690:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1688 |         }
1689 | 
1690 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1691 |         return true
1692 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:2645:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2643 |         }
2644 |         if let textView = firstResponder as? NSTextView,
2645 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2646 |            field.accessibilityIdentifier() == identifier
2647 |         {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:10904:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10902 |         newName: String
10903 |     ) {
10904 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10905 |               let rename = current.rename,
10906 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14357:23: warning: no 'async' operations occur within 'await' expression
14355 |                 }
14356 | 
14357 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14358 |                     return
14359 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14370:35: warning: no 'async' operations occur within 'await' expression
14368 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14369 |                         && parse.reportsClipDirective
14370 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14371 |                         draft: draft,
14372 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14385:27: warning: no 'async' operations occur within 'await' expression
14383 |                     await completionGate.value
14384 |                     try Task.checkCancellation()
14385 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14386 |                         return
14387 |                     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14392:20: warning: no 'async' operations occur within 'await' expression
14390 |                 if let cursorUTF8Offset,
14391 |                    requestCompletion,
14392 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14393 |                        parse: parse,
14394 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14398:37: warning: no 'async' operations occur within 'await' expression
14396 |                    ) == true
14397 |                 {
14398 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14399 |                         parse: parse,
14400 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTransferFailureCardView.swift:129:17: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
127 |             result =
128 |                 result
129 |                 + Text(String(characters[lower..<upper]))
    |                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
130 |                 .foregroundColor(formColor(segment.part))
131 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
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
Build of product 'BobMacCapture' complete! (217.89s)
/tmp/bob-mac-capture-flip/.build/bundle/Bob Mac Capture.app/Contents/MacOS/BobMacCapture: replacing existing signature
/tmp/bob-mac-capture-flip/.build/bundle/Bob Mac Capture.app: replacing existing signature
/tmp/bob-mac-capture-flip/.build/bundle/Bob Mac Capture.app
./Scripts/typecheck-tests.sh
Building for debugging...
[0/18] Write sources
[5/18] Write refs-rank-entitlement.plist
[5/18] Write BobMacCapture-entitlement.plist
[5/18] Write BobMacCaptureInstallHelper-entitlement.plist
[8/18] Write swift-version--1AB21518FC5DEDBE.txt
[10/103] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[11/103] Compiling CaptureCore BlockIDPickerIndex.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[12/103] Compiling CaptureCore BlockIDRules.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[13/103] Compiling CaptureCore BobEnvironment.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[14/103] Compiling CaptureCore BobErrors.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[15/103] Compiling CaptureCore BobExecutableResolver.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[16/103] Compiling CaptureCore BobMacCaptureLaunchContext.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[17/103] Compiling CaptureCore BobProcessClient.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[18/103] Compiling CaptureCore CanceledDraftStashStore.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[19/103] Compiling CaptureCore CaptureAgendaBoundaryRefresh.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[20/103] Compiling CaptureCore CaptureAgendaFitPlanner.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[21/103] Compiling CaptureCore CaptureAgendaHold.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[22/103] Emitting module CaptureCore
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[23/103] Compiling CaptureCore CaptureOpenPlan.swift
[24/103] Compiling CaptureCore CapturePanelPlacement.swift
[25/103] Compiling CaptureCore CapturePastBoundary.swift
[26/103] Compiling CaptureCore CapturePickerHelpers.swift
[27/103] Compiling CaptureCore CapturePickerPresentation.swift
[28/103] Compiling CaptureCore CapturePlanBudgetPresentation.swift
[29/103] Compiling CaptureCore CapturePomodoroAdjustPresentation.swift
[30/103] Compiling CaptureCore CapturePomodoroBlockPresentation.swift
[31/103] Compiling CaptureCore CapturePomodoroClosePresentation.swift
[32/103] Compiling CaptureCore CapturePomodoroLineTokens.swift
[33/103] Compiling CaptureCore CapturePomodoroLinkPresentation.swift
[34/103] Compiling CaptureCore CapturePomodoroMergePresentation.swift
[35/115] Compiling CaptureCore ObsidianOpenURL.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[36/115] Compiling CaptureCore ParentTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[37/115] Compiling CaptureCore PomodoroHomes.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[38/115] Compiling CaptureCore ProjectTaskMovePickerPresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[39/115] Compiling CaptureCore SimilarTasksBandEdits.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[40/115] Compiling CaptureCore SimilarTasksBandPolicy.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[41/115] Compiling CaptureCore SimilarTasksBandPresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[42/115] Compiling CaptureCore TaskCompletePickerPresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[43/115] Compiling CaptureCore TaskDisplayText.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[44/115] Compiling CaptureCore TaskLinkPickerPresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[45/115] Compiling CaptureCore WikilinkTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[46/115] Compiling CaptureCore WorkBadgeTone.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[47/115] Compiling CaptureCore CaptureRelationHeldPresentation.swift
[48/115] Compiling CaptureCore CaptureRelationSuccessorModels.swift
[49/115] Compiling CaptureCore CaptureRelationshipCopy.swift
[50/115] Compiling CaptureCore CaptureRelationshipPresentation.swift
[51/115] Compiling CaptureCore CaptureSavedTemplates.swift
[52/115] Compiling CaptureCore CaptureSubBulletPresentation.swift
[53/115] Compiling CaptureCore CaptureSuccessorOfferRows.swift
[54/115] Compiling CaptureCore CaptureSuccessorPresentation.swift
[55/115] Compiling CaptureCore CaptureTargetsCache.swift
[56/115] Compiling CaptureCore CaptureTaskBlockPresentation.swift
[57/115] Compiling CaptureCore CaptureTaskCompletePresentation.swift
[58/115] Compiling CaptureCore CaptureTaskGotoScopeState.swift
[59/115] Compiling CaptureCore CaptureAgendaInlineText.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[60/115] Compiling CaptureCore CaptureAgendaLayout.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[61/115] Compiling CaptureCore CaptureAgendaModels.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[62/115] Compiling CaptureCore CaptureAgendaPresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[63/115] Compiling CaptureCore CaptureAgendaRefreshFilter.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[64/115] Compiling CaptureCore CaptureAgendaRefreshState.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[65/115] Compiling CaptureCore CaptureAgendaVisibility.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[66/115] Compiling CaptureCore CaptureBlockDiffRow.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[67/115] Compiling CaptureCore CaptureBlockIDSplice.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[68/115] Compiling CaptureCore CaptureClipPresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[69/115] Compiling CaptureCore CaptureCloseTaskCommaAssist.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[70/115] Compiling CaptureCore CaptureCloseTaskCommaProvenance.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[71/115] Compiling CaptureCore CaptureCompletionMenu.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9431:13: warning: no calls to throwing functions occur within 'try' expression
 9429 |         let container = try decoder.singleValueContainer()
 9430 |         // Explicit null has no value; treat it as absent.
 9431 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9432 |             throw DecodingError.valueNotFound(
 9433 |                 CaptureThemeSuggestion.self,
[72/115] Compiling CaptureCore CaptureDrawerMenuPresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9431:13: warning: no calls to throwing functions occur within 'try' expression
 9429 |         let container = try decoder.singleValueContainer()
 9430 |         // Explicit null has no value; treat it as absent.
 9431 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9432 |             throw DecodingError.valueNotFound(
 9433 |                 CaptureThemeSuggestion.self,
[73/115] Compiling CaptureCore CaptureEditWrite.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9431:13: warning: no calls to throwing functions occur within 'try' expression
 9429 |         let container = try decoder.singleValueContainer()
 9430 |         // Explicit null has no value; treat it as absent.
 9431 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9432 |             throw DecodingError.valueNotFound(
 9433 |                 CaptureThemeSuggestion.self,
[74/115] Compiling CaptureCore CaptureGrammarGate.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9431:13: warning: no calls to throwing functions occur within 'try' expression
 9429 |         let container = try decoder.singleValueContainer()
 9430 |         // Explicit null has no value; treat it as absent.
 9431 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9432 |             throw DecodingError.valueNotFound(
 9433 |                 CaptureThemeSuggestion.self,
[75/115] Compiling CaptureCore CaptureInboxRoutePresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9431:13: warning: no calls to throwing functions occur within 'try' expression
 9429 |         let container = try decoder.singleValueContainer()
 9430 |         // Explicit null has no value; treat it as absent.
 9431 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9432 |             throw DecodingError.valueNotFound(
 9433 |                 CaptureThemeSuggestion.self,
[76/115] Compiling CaptureCore CaptureLineCaseToggle.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9431:13: warning: no calls to throwing functions occur within 'try' expression
 9429 |         let container = try decoder.singleValueContainer()
 9430 |         // Explicit null has no value; treat it as absent.
 9431 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9432 |             throw DecodingError.valueNotFound(
 9433 |                 CaptureThemeSuggestion.self,
[77/115] Compiling CaptureCore CaptureLinkGuardPresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9431:13: warning: no calls to throwing functions occur within 'try' expression
 9429 |         let container = try decoder.singleValueContainer()
 9430 |         // Explicit null has no value; treat it as absent.
 9431 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9432 |             throw DecodingError.valueNotFound(
 9433 |                 CaptureThemeSuggestion.self,
[78/115] Compiling CaptureCore CaptureList.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9431:13: warning: no calls to throwing functions occur within 'try' expression
 9429 |         let container = try decoder.singleValueContainer()
 9430 |         // Explicit null has no value; treat it as absent.
 9431 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9432 |             throw DecodingError.valueNotFound(
 9433 |                 CaptureThemeSuggestion.self,
[79/115] Compiling CaptureCore CaptureModels.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9431:13: warning: no calls to throwing functions occur within 'try' expression
 9429 |         let container = try decoder.singleValueContainer()
 9430 |         // Explicit null has no value; treat it as absent.
 9431 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9432 |             throw DecodingError.valueNotFound(
 9433 |                 CaptureThemeSuggestion.self,
[80/115] Compiling CaptureCore CaptureMoveChoicePresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9431:13: warning: no calls to throwing functions occur within 'try' expression
 9429 |         let container = try decoder.singleValueContainer()
 9430 |         // Explicit null has no value; treat it as absent.
 9431 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9432 |             throw DecodingError.valueNotFound(
 9433 |                 CaptureThemeSuggestion.self,
[81/115] Compiling CaptureCore CaptureNotePullPresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9431:13: warning: no calls to throwing functions occur within 'try' expression
 9429 |         let container = try decoder.singleValueContainer()
 9430 |         // Explicit null has no value; treat it as absent.
 9431 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9432 |             throw DecodingError.valueNotFound(
 9433 |                 CaptureThemeSuggestion.self,
[82/115] Compiling CaptureCore CaptureOpenHintPresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9431:13: warning: no calls to throwing functions occur within 'try' expression
 9429 |         let container = try decoder.singleValueContainer()
 9430 |         // Explicit null has no value; treat it as absent.
 9431 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9432 |             throw DecodingError.valueNotFound(
 9433 |                 CaptureThemeSuggestion.self,
[83/115] Compiling CaptureCore CaptureTaskThemePresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[84/115] Compiling CaptureCore CaptureTaskTypeMenuPresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[85/115] Compiling CaptureCore CaptureTextRanges.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[86/115] Compiling CaptureCore CaptureTodayPomodoroGoto.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[87/115] Compiling CaptureCore CaptureTogglePresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[88/115] Compiling CaptureCore CaptureTransferFailurePresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[89/115] Compiling CaptureCore CaptureTransferPresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[90/115] Compiling CaptureCore CaptureUnconfiguredThemePresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[91/115] Compiling CaptureCore CaptureWordMotion.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[92/115] Compiling CaptureCore CompletionRowContent.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[93/115] Compiling CaptureCore DependencyPickerPresentation.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[94/115] Compiling CaptureCore FuzzyMatcher.swift
/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-flip/Sources/CaptureCore/CaptureModels.swift:9632:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9630 | }
 9631 | 
 9632 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9633 |     public let replacement: String
 9634 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[95/115] Compiling CaptureCore CapturePomodoroPastPresentation.swift
[96/115] Compiling CaptureCore CapturePomodoroResetPresentation.swift
[97/115] Compiling CaptureCore CapturePomodoroShiftPresentation.swift
[98/115] Compiling CaptureCore CapturePomodoroSplitPresentation.swift
[99/115] Compiling CaptureCore CapturePomodoroStartPresentation.swift
[100/115] Compiling CaptureCore CaptureProjectNotePresentation.swift
[101/115] Compiling CaptureCore CaptureRefFileUnder.swift
[102/115] Compiling CaptureCore CaptureRefPresentation.swift
[103/115] Compiling CaptureCore CaptureRelatedModels.swift
[104/115] Compiling CaptureCore CaptureRelationCancelPresentation.swift
[105/115] Compiling CaptureCore CaptureRelationCloseEffect.swift
[106/115] Compiling CaptureCore CaptureRelationCompletePresentation.swift
[107/151] Compiling RefsCore RefsNew.swift
[108/151] Compiling RefsCore RefsNewest.swift
[109/151] Compiling RefsCore RefsPDFUpdates.swift
[110/151] Compiling RefsCore RefsPanelGeometry.swift
[111/155] Compiling RefsCore RefsStores.swift
/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 41 | 
 42 |     private let fileURL: URL
 43 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 |     private let onError: @Sendable (String) -> Void
 45 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
182 | 
183 |     private let fileURL: URL
184 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
185 |     private let onError: @Sendable (String) -> Void
186 |     private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
376 | 
377 |     private let fileURL: URL
378 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
379 |     private let onError: @Sendable (String) -> Void
380 |     private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[112/155] Compiling RefsCore RefsTabClose.swift
/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 41 | 
 42 |     private let fileURL: URL
 43 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 |     private let onError: @Sendable (String) -> Void
 45 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
182 | 
183 |     private let fileURL: URL
184 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
185 |     private let onError: @Sendable (String) -> Void
186 |     private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
376 | 
377 |     private let fileURL: URL
378 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
379 |     private let onError: @Sendable (String) -> Void
380 |     private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[113/155] Compiling RefsCore RefsTabsRanking.swift
/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 41 | 
 42 |     private let fileURL: URL
 43 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 |     private let onError: @Sendable (String) -> Void
 45 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
182 | 
183 |     private let fileURL: URL
184 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
185 |     private let onError: @Sendable (String) -> Void
186 |     private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
376 | 
377 |     private let fileURL: URL
378 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
379 |     private let onError: @Sendable (String) -> Void
380 |     private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[114/155] Compiling RefsCore RefsToday.swift
/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 41 | 
 42 |     private let fileURL: URL
 43 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 |     private let onError: @Sendable (String) -> Void
 45 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
182 | 
183 |     private let fileURL: URL
184 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
185 |     private let onError: @Sendable (String) -> Void
186 |     private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
376 | 
377 |     private let fileURL: URL
378 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
379 |     private let onError: @Sendable (String) -> Void
380 |     private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[115/155] Compiling RefsCore RefsScan.swift
[116/155] Compiling RefsCore RefsScanReceipt.swift
[117/155] Compiling RefsCore RefsSectionedWindow.swift
[118/155] Compiling RefsCore RefsSelection.swift
[119/155] Emitting module RefsCore
/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 41 | 
 42 |     private let fileURL: URL
 43 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
 44 |     private let onError: @Sendable (String) -> Void
 45 | 

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
182 | 
183 |     private let fileURL: URL
184 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
185 |     private let onError: @Sendable (String) -> Void
186 |     private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.

/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
376 | 
377 |     private let fileURL: URL
378 |     private let fileManager: FileManager
    |                 `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
379 |     private let onError: @Sendable (String) -> Void
380 |     private let now: @Sendable () -> Date

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/Foundation.framework/Headers/NSFileManager.h:96:12: note: class 'FileManager' does not conform to the 'Sendable' protocol
 94 | extern NSNotificationName const NSUbiquityIdentityDidChangeNotification API_AVAILABLE(macos(10.8), ios(6.0), watchos(2.0), tvos(9.0));
 95 | 
 96 | @interface NSFileManager : NSObject
    |            `- note: class 'FileManager' does not conform to the 'Sendable' protocol
 97 | 
 98 | /* Returns the default singleton instance.
[120/155] Compiling RefsCore RefsInspectorImages.swift
[121/155] Compiling RefsCore RefsLinks.swift
[122/155] Compiling RefsCore RefsListScroll.swift
[123/155] Compiling RefsCore RefsModel.swift
[124/155] Compiling RefsCore RefsPickerScope.swift
/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[125/155] Compiling RefsCore RefsQuoteUnderline.swift
/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[126/155] Compiling RefsCore RefsRanking.swift
/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[127/155] Compiling RefsCore RefsRename.swift
/private/tmp/bob-mac-capture-flip/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[128/155] Compiling RefsCore RefsDecoding.swift
[129/155] Compiling RefsCore RefsFetching.swift
[130/155] Compiling RefsCore RefsHighlightPicker.swift
[131/155] Compiling RefsCore RefsHighlightsTabs.swift
[132/155] Compiling RefsCore RefsInspector.swift
[133/155] Compiling RefsCore HighlightsSaveScan.swift
[134/155] Compiling RefsCore RefsArrivals.swift
[135/155] Compiling RefsCore RefsCaption.swift
[136/155] Compiling RefsCore RefsCode.swift
[137/155] Compiling RefsCore RefsCopy.swift
[138/155] Compiling RefsCore RefsTodayLinkCard.swift
[139/155] Compiling RefsCore RefsTodayLinkModels.swift
[140/155] Compiling RefsCore RefsTodayLinkPresentation.swift
[141/155] Compiling RefsCore RefsWatcherRelevance.swift
[142/241] Emitting module refs_rank
[143/241] Compiling refs_rank main.swift
[143/241] Write Objects.LinkFileList
[144/241] Linking refs-rank
[145/241] Applying refs-rank
[147/241] Emitting module BobMacCaptureInstallHelper
[148/241] Compiling BobMacCaptureInstallHelper InstallRelauncher.swift
[149/241] Compiling BobMacCaptureInstallHelper InstallHelperError.swift
[150/241] Compiling BobMacCaptureInstallHelper InstallHelperArguments.swift
[151/241] Compiling BobMacCaptureInstallHelper BobMacCaptureInstallHelperMain.swift
[151/241] Write Objects.LinkFileList
[152/241] Linking BobMacCaptureInstallHelper
[153/241] Applying BobMacCaptureInstallHelper
[155/241] Emitting module BobMacCapture
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1094 |         }
1095 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1094 |         }
1095 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
269 |     static let refsHighlightsCodeKey = "refsHighlightsCodeKey"
270 |     static let refsHighlightsLinkKey = "refsHighlightsLinkKey"
271 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
272 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
273 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:84:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         processClient: BobProcessClient? = nil,
 83 |         vaultRootPath: String = "",
 84 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 85 |         now: @Sendable @escaping () -> Date = { Date() },
 86 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[156/252] Compiling BobMacCapture RefsTabsViews.swift
[157/252] Compiling BobMacCapture RefsTodayLinkCardView.swift
[158/252] Compiling BobMacCapture RefsUnderlineRenderer.swift
[159/252] Compiling BobMacCapture RefsVisualTokens.swift
[160/252] Compiling BobMacCapture RefsAliasHotkeyRegistration.swift
[161/252] Compiling BobMacCapture RefsHighlightsCodeKey.swift
[162/252] Compiling BobMacCapture RefsHighlightsCopyKey.swift
[163/252] Compiling BobMacCapture RefsHighlightsLinkKey.swift
[164/252] Compiling BobMacCapture RefsHighlightsOpenKey.swift
[165/252] Compiling BobMacCapture RefsHighlightsTabsKey.swift
[166/252] Compiling BobMacCapture RefsHotkeyRegistration.swift
[167/252] Compiling BobMacCapture AccessibilityTrust.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1094 |         }
1095 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1094 |         }
1095 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  81 |         NSApplication.shared.addSceneRepresentation(representation)
  82 |         settingsSceneRepresentation = representation
  83 |         settingsPresentation = SettingsPresentation {
     |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  84 |             representation.environment.openSettings()
  85 |         }
     :
1088 |     var activateApplication: () -> Void
1089 | 
1090 |     init(
     |     `- note: 'init(openSettings:activateApplication:)' declared here
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:84:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         processClient: BobProcessClient? = nil,
 83 |         vaultRootPath: String = "",
 84 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 85 |         now: @Sendable @escaping () -> Date = { Date() },
 86 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
269 |     static let refsHighlightsCodeKey = "refsHighlightsCodeKey"
270 |     static let refsHighlightsLinkKey = "refsHighlightsLinkKey"
271 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
272 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
273 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:422:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
420 |                 Task { [weak self] in
421 |                     await MainActor.run {
422 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
423 |                     }
424 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[168/252] Compiling BobMacCapture AppDelegate.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1094 |         }
1095 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1094 |         }
1095 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  81 |         NSApplication.shared.addSceneRepresentation(representation)
  82 |         settingsSceneRepresentation = representation
  83 |         settingsPresentation = SettingsPresentation {
     |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  84 |             representation.environment.openSettings()
  85 |         }
     :
1088 |     var activateApplication: () -> Void
1089 | 
1090 |     init(
     |     `- note: 'init(openSettings:activateApplication:)' declared here
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:84:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         processClient: BobProcessClient? = nil,
 83 |         vaultRootPath: String = "",
 84 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 85 |         now: @Sendable @escaping () -> Date = { Date() },
 86 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
269 |     static let refsHighlightsCodeKey = "refsHighlightsCodeKey"
270 |     static let refsHighlightsLinkKey = "refsHighlightsLinkKey"
271 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
272 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
273 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:422:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
420 |                 Task { [weak self] in
421 |                     await MainActor.run {
422 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
423 |                     }
424 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[169/252] Compiling BobMacCapture AppRelauncher.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1094 |         }
1095 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1094 |         }
1095 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  81 |         NSApplication.shared.addSceneRepresentation(representation)
  82 |         settingsSceneRepresentation = representation
  83 |         settingsPresentation = SettingsPresentation {
     |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  84 |             representation.environment.openSettings()
  85 |         }
     :
1088 |     var activateApplication: () -> Void
1089 | 
1090 |     init(
     |     `- note: 'init(openSettings:activateApplication:)' declared here
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:84:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         processClient: BobProcessClient? = nil,
 83 |         vaultRootPath: String = "",
 84 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 85 |         now: @Sendable @escaping () -> Date = { Date() },
 86 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
269 |     static let refsHighlightsCodeKey = "refsHighlightsCodeKey"
270 |     static let refsHighlightsLinkKey = "refsHighlightsLinkKey"
271 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
272 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
273 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:422:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
420 |                 Task { [weak self] in
421 |                     await MainActor.run {
422 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
423 |                     }
424 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[170/252] Compiling BobMacCapture AppSettings.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1094 |         }
1095 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1094 |         }
1095 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  81 |         NSApplication.shared.addSceneRepresentation(representation)
  82 |         settingsSceneRepresentation = representation
  83 |         settingsPresentation = SettingsPresentation {
     |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  84 |             representation.environment.openSettings()
  85 |         }
     :
1088 |     var activateApplication: () -> Void
1089 | 
1090 |     init(
     |     `- note: 'init(openSettings:activateApplication:)' declared here
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:84:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         processClient: BobProcessClient? = nil,
 83 |         vaultRootPath: String = "",
 84 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 85 |         now: @Sendable @escaping () -> Date = { Date() },
 86 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
269 |     static let refsHighlightsCodeKey = "refsHighlightsCodeKey"
270 |     static let refsHighlightsLinkKey = "refsHighlightsLinkKey"
271 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
272 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
273 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:422:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
420 |                 Task { [weak self] in
421 |                     await MainActor.run {
422 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
423 |                     }
424 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[171/252] Compiling BobMacCapture BlockDiffCard.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1094 |         }
1095 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1094 |         }
1095 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  81 |         NSApplication.shared.addSceneRepresentation(representation)
  82 |         settingsSceneRepresentation = representation
  83 |         settingsPresentation = SettingsPresentation {
     |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  84 |             representation.environment.openSettings()
  85 |         }
     :
1088 |     var activateApplication: () -> Void
1089 | 
1090 |     init(
     |     `- note: 'init(openSettings:activateApplication:)' declared here
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:84:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         processClient: BobProcessClient? = nil,
 83 |         vaultRootPath: String = "",
 84 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 85 |         now: @Sendable @escaping () -> Date = { Date() },
 86 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
269 |     static let refsHighlightsCodeKey = "refsHighlightsCodeKey"
270 |     static let refsHighlightsLinkKey = "refsHighlightsLinkKey"
271 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
272 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
273 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:422:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
420 |                 Task { [weak self] in
421 |                     await MainActor.run {
422 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
423 |                     }
424 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[172/252] Compiling BobMacCapture BlockIDField.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1094 |         }
1095 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1094 |         }
1095 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  81 |         NSApplication.shared.addSceneRepresentation(representation)
  82 |         settingsSceneRepresentation = representation
  83 |         settingsPresentation = SettingsPresentation {
     |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  84 |             representation.environment.openSettings()
  85 |         }
     :
1088 |     var activateApplication: () -> Void
1089 | 
1090 |     init(
     |     `- note: 'init(openSettings:activateApplication:)' declared here
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:84:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         processClient: BobProcessClient? = nil,
 83 |         vaultRootPath: String = "",
 84 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 85 |         now: @Sendable @escaping () -> Date = { Date() },
 86 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
269 |     static let refsHighlightsCodeKey = "refsHighlightsCodeKey"
270 |     static let refsHighlightsLinkKey = "refsHighlightsLinkKey"
271 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
272 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
273 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:422:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
420 |                 Task { [weak self] in
421 |                     await MainActor.run {
422 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
423 |                     }
424 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[173/252] Compiling BobMacCapture BobMacCaptureMain.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1094 |         }
1095 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1094 |         }
1095 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  81 |         NSApplication.shared.addSceneRepresentation(representation)
  82 |         settingsSceneRepresentation = representation
  83 |         settingsPresentation = SettingsPresentation {
     |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  84 |             representation.environment.openSettings()
  85 |         }
     :
1088 |     var activateApplication: () -> Void
1089 | 
1090 |     init(
     |     `- note: 'init(openSettings:activateApplication:)' declared here
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:84:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         processClient: BobProcessClient? = nil,
 83 |         vaultRootPath: String = "",
 84 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 85 |         now: @Sendable @escaping () -> Date = { Date() },
 86 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
269 |     static let refsHighlightsCodeKey = "refsHighlightsCodeKey"
270 |     static let refsHighlightsLinkKey = "refsHighlightsLinkKey"
271 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
272 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
273 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:422:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
420 |                 Task { [weak self] in
421 |                     await MainActor.run {
422 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
423 |                     }
424 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[174/252] Compiling BobMacCapture BobPanelCoordinator.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1094 |         }
1095 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1094 |         }
1095 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  81 |         NSApplication.shared.addSceneRepresentation(representation)
  82 |         settingsSceneRepresentation = representation
  83 |         settingsPresentation = SettingsPresentation {
     |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  84 |             representation.environment.openSettings()
  85 |         }
     :
1088 |     var activateApplication: () -> Void
1089 | 
1090 |     init(
     |     `- note: 'init(openSettings:activateApplication:)' declared here
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:84:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         processClient: BobProcessClient? = nil,
 83 |         vaultRootPath: String = "",
 84 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 85 |         now: @Sendable @escaping () -> Date = { Date() },
 86 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
269 |     static let refsHighlightsCodeKey = "refsHighlightsCodeKey"
270 |     static let refsHighlightsLinkKey = "refsHighlightsLinkKey"
271 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
272 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
273 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:422:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
420 |                 Task { [weak self] in
421 |                     await MainActor.run {
422 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
423 |                     }
424 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[175/252] Compiling BobMacCapture BundleSigningInspector.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1094 |         }
1095 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1094 |         }
1095 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  81 |         NSApplication.shared.addSceneRepresentation(representation)
  82 |         settingsSceneRepresentation = representation
  83 |         settingsPresentation = SettingsPresentation {
     |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  84 |             representation.environment.openSettings()
  85 |         }
     :
1088 |     var activateApplication: () -> Void
1089 | 
1090 |     init(
     |     `- note: 'init(openSettings:activateApplication:)' declared here
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:84:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         processClient: BobProcessClient? = nil,
 83 |         vaultRootPath: String = "",
 84 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 85 |         now: @Sendable @escaping () -> Date = { Date() },
 86 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
269 |     static let refsHighlightsCodeKey = "refsHighlightsCodeKey"
270 |     static let refsHighlightsLinkKey = "refsHighlightsLinkKey"
271 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
272 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
273 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:422:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
420 |                 Task { [weak self] in
421 |                     await MainActor.run {
422 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
423 |                     }
424 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[176/252] Compiling BobMacCapture CanceledDraftStash.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1094 |         }
1095 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1094 |         }
1095 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  81 |         NSApplication.shared.addSceneRepresentation(representation)
  82 |         settingsSceneRepresentation = representation
  83 |         settingsPresentation = SettingsPresentation {
     |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  84 |             representation.environment.openSettings()
  85 |         }
     :
1088 |     var activateApplication: () -> Void
1089 | 
1090 |     init(
     |     `- note: 'init(openSettings:activateApplication:)' declared here
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:84:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         processClient: BobProcessClient? = nil,
 83 |         vaultRootPath: String = "",
 84 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 85 |         now: @Sendable @escaping () -> Date = { Date() },
 86 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
269 |     static let refsHighlightsCodeKey = "refsHighlightsCodeKey"
270 |     static let refsHighlightsLinkKey = "refsHighlightsLinkKey"
271 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
272 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
273 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:422:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
420 |                 Task { [weak self] in
421 |                     await MainActor.run {
422 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
423 |                     }
424 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[177/252] Compiling BobMacCapture CaptureAgendaRowMeasurer.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1094 |         }
1095 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1094 |         }
1095 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  81 |         NSApplication.shared.addSceneRepresentation(representation)
  82 |         settingsSceneRepresentation = representation
  83 |         settingsPresentation = SettingsPresentation {
     |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  84 |             representation.environment.openSettings()
  85 |         }
     :
1088 |     var activateApplication: () -> Void
1089 | 
1090 |     init(
     |     `- note: 'init(openSettings:activateApplication:)' declared here
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:84:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         processClient: BobProcessClient? = nil,
 83 |         vaultRootPath: String = "",
 84 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 85 |         now: @Sendable @escaping () -> Date = { Date() },
 86 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
269 |     static let refsHighlightsCodeKey = "refsHighlightsCodeKey"
270 |     static let refsHighlightsLinkKey = "refsHighlightsLinkKey"
271 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
272 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
273 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:422:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
420 |                 Task { [weak self] in
421 |                     await MainActor.run {
422 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
423 |                     }
424 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[178/252] Compiling BobMacCapture CaptureAgendaStore.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                                  `- warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
1094 |         }
1095 |     ) {

AppKit.NSApplication.activate:3:24: note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
1 | class NSApplication {
2 | @available(macOS 14.0, *)
3 |   @MainActor open func activate()}
  |                        |- note: calls to instance method 'activate()' from outside of its actor context are implicitly asynchronous
  |                        `- note: main actor isolation inferred from inheritance from class 'NSResponder'
4 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {
1093 |             NSApplication.shared.activate()
     |                           `- warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
1094 |         }
1095 |     ) {

/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/System/Library/Frameworks/AppKit.framework/Headers/NSApplication.h:193:61: note: class property declared here
191 | APPKIT_EXTERN __kindof NSApplication * _Null_unspecified NSApp NS_SWIFT_UI_ACTOR;
192 | 
193 | @property (class, readonly, strong) __kindof NSApplication *sharedApplication;
    |                                                             `- note: class property declared here
194 | @property (nullable, weak) id<NSApplicationDelegate> delegate;
195 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  81 |         NSApplication.shared.addSceneRepresentation(representation)
  82 |         settingsSceneRepresentation = representation
  83 |         settingsPresentation = SettingsPresentation {
     |                                                     `- warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
  84 |             representation.environment.openSettings()
  85 |         }
     :
1088 |     var activateApplication: () -> Void
1089 | 
1090 |     init(
     |     `- note: 'init(openSettings:activateApplication:)' declared here
1091 |         openSettings: @escaping () -> Void = {},
1092 |         activateApplication: @escaping () -> Void = {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:84:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         processClient: BobProcessClient? = nil,
 83 |         vaultRootPath: String = "",
 84 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 85 |         now: @Sendable @escaping () -> Date = { Date() },
 86 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {
    :
269 |     static let refsHighlightsCodeKey = "refsHighlightsCodeKey"
270 |     static let refsHighlightsLinkKey = "refsHighlightsLinkKey"
271 |     static let refsHighlightsAppPath = AppSettings.refsHighlightsAppPathKey
    |                                                    `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
272 |     static let canceledDraftStashCapacity = "canceledDraftStashCapacity"
273 |     static let refsInspectorNotesPageSize = "refsInspectorNotesPageSize"

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaStore.swift:422:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
420 |                 Task { [weak self] in
421 |                     await MainActor.run {
422 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
423 |                     }
424 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[179/252] Compiling BobMacCapture CaptureTransferFailureCardView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTransferFailureCardView.swift:129:17: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
127 |             result =
128 |                 result
129 |                 + Text(String(characters[lower..<upper]))
    |                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
130 |                 .foregroundColor(formColor(segment.part))
131 |         }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[180/252] Compiling BobMacCapture ClipCardView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTransferFailureCardView.swift:129:17: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
127 |             result =
128 |                 result
129 |                 + Text(String(characters[lower..<upper]))
    |                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
130 |                 .foregroundColor(formColor(segment.part))
131 |         }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[181/252] Compiling BobMacCapture HighlightsSaveKeyMonitor.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTransferFailureCardView.swift:129:17: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
127 |             result =
128 |                 result
129 |                 + Text(String(characters[lower..<upper]))
    |                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
130 |                 .foregroundColor(formColor(segment.part))
131 |         }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[182/252] Compiling BobMacCapture HighlightsTakeover.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTransferFailureCardView.swift:129:17: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
127 |             result =
128 |                 result
129 |                 + Text(String(characters[lower..<upper]))
    |                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
130 |                 .foregroundColor(formColor(segment.part))
131 |         }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[183/252] Compiling BobMacCapture HotKeyRegistry.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTransferFailureCardView.swift:129:17: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
127 |             result =
128 |                 result
129 |                 + Text(String(characters[lower..<upper]))
    |                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
130 |                 .foregroundColor(formColor(segment.part))
131 |         }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[184/252] Compiling BobMacCapture NotificationService.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTransferFailureCardView.swift:129:17: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
127 |             result =
128 |                 result
129 |                 + Text(String(characters[lower..<upper]))
    |                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
130 |                 .foregroundColor(formColor(segment.part))
131 |         }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[185/252] Compiling BobMacCapture PlainTextPaste.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTransferFailureCardView.swift:129:17: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
127 |             result =
128 |                 result
129 |                 + Text(String(characters[lower..<upper]))
    |                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
130 |                 .foregroundColor(formColor(segment.part))
131 |         }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[186/252] Compiling BobMacCapture PomodoroBlockView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTransferFailureCardView.swift:129:17: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
127 |             result =
128 |                 result
129 |                 + Text(String(characters[lower..<upper]))
    |                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
130 |                 .foregroundColor(formColor(segment.part))
131 |         }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[187/252] Compiling BobMacCapture PomodoroHomeColor.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTransferFailureCardView.swift:129:17: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
127 |             result =
128 |                 result
129 |                 + Text(String(characters[lower..<upper]))
    |                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
130 |                 .foregroundColor(formColor(segment.part))
131 |         }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[188/252] Compiling BobMacCapture PomodoroNameField.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTransferFailureCardView.swift:129:17: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
127 |             result =
128 |                 result
129 |                 + Text(String(characters[lower..<upper]))
    |                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
130 |                 .foregroundColor(formColor(segment.part))
131 |         }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[189/252] Compiling BobMacCapture PomodoroThemeViews.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTransferFailureCardView.swift:129:17: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
127 |             result =
128 |                 result
129 |                 + Text(String(characters[lower..<upper]))
    |                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
130 |                 .foregroundColor(formColor(segment.part))
131 |         }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[190/252] Compiling BobMacCapture AXHighlightsTabsReader.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTransferFailureCardView.swift:129:17: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
127 |             result =
128 |                 result
129 |                 + Text(String(characters[lower..<upper]))
    |                 `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
130 |                 .foregroundColor(formColor(segment.part))
131 |         }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[191/252] Compiling BobMacCapture RelationLabelField.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[192/252] Compiling BobMacCapture SavedTemplateShelf.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[193/252] Compiling BobMacCapture SectionBlockView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[194/252] Compiling BobMacCapture SettingsView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[195/252] Compiling BobMacCapture Signposts.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[196/252] Compiling BobMacCapture SimilarTasksBandView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[197/252] Compiling BobMacCapture StatusItemController.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[198/252] Compiling BobMacCapture StatusItemGlyph.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[199/252] Compiling BobMacCapture TaskBlockView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[200/252] Compiling BobMacCapture TodayBadge.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[201/252] Compiling BobMacCapture VaultTargetWatcher.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[202/252] Compiling BobMacCapture RefsActionsMenu.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[203/252] Compiling BobMacCapture RefsAnnotationImages.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[204/252] Compiling BobMacCapture RefsCodePreviewWell.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[205/252] Compiling BobMacCapture RefsCopyCardView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[206/252] Compiling BobMacCapture RefsCopyHUD.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[207/252] Compiling BobMacCapture RefsFooter.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[208/252] Compiling BobMacCapture RefsInspectorImageViews.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[209/252] Compiling BobMacCapture RefsInspectorLoader.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[210/252] Compiling BobMacCapture RefsInspectorScroll.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[211/252] Compiling BobMacCapture RefsInspectorView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[212/252] Compiling BobMacCapture RefsKeyRouter.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[213/252] Compiling BobMacCapture RefsLibrary.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[214/252] Compiling BobMacCapture CapturePanelWindowSizer.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[215/252] Compiling BobMacCapture CapturePickerFilterField.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[216/252] Compiling BobMacCapture CapturePickerState.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[217/252] Compiling BobMacCapture CapturePickerView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[218/252] Compiling BobMacCapture CapturePlanBudgetMeterRow.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[219/252] Compiling BobMacCapture CapturePullInChoice.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[220/252] Compiling BobMacCapture CapturePullInChoiceView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[221/252] Compiling BobMacCapture CaptureShowRefreshWindow.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[222/252] Compiling BobMacCapture CaptureSnippetResolver.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[223/252] Compiling BobMacCapture CaptureTargetsRefreshGate.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[224/252] Compiling BobMacCapture CaptureTaskTypeMenuView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[225/252] Compiling BobMacCapture CaptureTransferCardView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[226/252] Compiling BobMacCapture RefsLinkPreviewWell.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[227/252] Compiling BobMacCapture RefsListView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[228/252] Compiling BobMacCapture RefsPanel.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[229/252] Compiling BobMacCapture RefsPanelModel.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[230/252] Compiling BobMacCapture RefsPanelStates.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[231/252] Compiling BobMacCapture RefsPanelView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[232/252] Compiling BobMacCapture RefsPickerScopeViews.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[233/252] Compiling BobMacCapture RefsQuoteText.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[234/252] Compiling BobMacCapture RefsRenameCardView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[235/252] Compiling BobMacCapture RefsRowView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[236/252] Compiling BobMacCapture RefsScanReceiptObserver.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[237/252] Compiling BobMacCapture RefsSearchBar.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[238/252] Compiling BobMacCapture CaptureAgendaView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:1690:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1688 |         }
1689 | 
1690 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1691 |         return true
1692 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:2645:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2643 |         }
2644 |         if let textView = firstResponder as? NSTextView,
2645 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2646 |            field.accessibilityIdentifier() == identifier
2647 |         {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:10904:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10902 |         newName: String
10903 |     ) {
10904 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10905 |               let rename = current.rename,
10906 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14357:23: warning: no 'async' operations occur within 'await' expression
14355 |                 }
14356 | 
14357 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14358 |                     return
14359 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14370:35: warning: no 'async' operations occur within 'await' expression
14368 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14369 |                         && parse.reportsClipDirective
14370 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14371 |                         draft: draft,
14372 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14385:27: warning: no 'async' operations occur within 'await' expression
14383 |                     await completionGate.value
14384 |                     try Task.checkCancellation()
14385 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14386 |                         return
14387 |                     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14392:20: warning: no 'async' operations occur within 'await' expression
14390 |                 if let cursorUTF8Offset,
14391 |                    requestCompletion,
14392 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14393 |                        parse: parse,
14394 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14398:37: warning: no 'async' operations occur within 'await' expression
14396 |                    ) == true
14397 |                 {
14398 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14399 |                         parse: parse,
14400 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[239/252] Compiling BobMacCapture CaptureAliasHotkeyRegistration.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:1690:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1688 |         }
1689 | 
1690 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1691 |         return true
1692 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:2645:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2643 |         }
2644 |         if let textView = firstResponder as? NSTextView,
2645 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2646 |            field.accessibilityIdentifier() == identifier
2647 |         {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:10904:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10902 |         newName: String
10903 |     ) {
10904 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10905 |               let rename = current.rename,
10906 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14357:23: warning: no 'async' operations occur within 'await' expression
14355 |                 }
14356 | 
14357 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14358 |                     return
14359 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14370:35: warning: no 'async' operations occur within 'await' expression
14368 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14369 |                         && parse.reportsClipDirective
14370 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14371 |                         draft: draft,
14372 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14385:27: warning: no 'async' operations occur within 'await' expression
14383 |                     await completionGate.value
14384 |                     try Task.checkCancellation()
14385 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14386 |                         return
14387 |                     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14392:20: warning: no 'async' operations occur within 'await' expression
14390 |                 if let cursorUTF8Offset,
14391 |                    requestCompletion,
14392 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14393 |                        parse: parse,
14394 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14398:37: warning: no 'async' operations occur within 'await' expression
14396 |                    ) == true
14397 |                 {
14398 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14399 |                         parse: parse,
14400 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[240/252] Compiling BobMacCapture CaptureDrawerMenuView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:1690:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1688 |         }
1689 | 
1690 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1691 |         return true
1692 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:2645:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2643 |         }
2644 |         if let textView = firstResponder as? NSTextView,
2645 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2646 |            field.accessibilityIdentifier() == identifier
2647 |         {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:10904:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10902 |         newName: String
10903 |     ) {
10904 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10905 |               let rename = current.rename,
10906 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14357:23: warning: no 'async' operations occur within 'await' expression
14355 |                 }
14356 | 
14357 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14358 |                     return
14359 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14370:35: warning: no 'async' operations occur within 'await' expression
14368 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14369 |                         && parse.reportsClipDirective
14370 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14371 |                         draft: draft,
14372 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14385:27: warning: no 'async' operations occur within 'await' expression
14383 |                     await completionGate.value
14384 |                     try Task.checkCancellation()
14385 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14386 |                         return
14387 |                     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14392:20: warning: no 'async' operations occur within 'await' expression
14390 |                 if let cursorUTF8Offset,
14391 |                    requestCompletion,
14392 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14393 |                        parse: parse,
14394 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14398:37: warning: no 'async' operations occur within 'await' expression
14396 |                    ) == true
14397 |                 {
14398 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14399 |                         parse: parse,
14400 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[241/252] Compiling BobMacCapture CaptureEditorPalette.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:1690:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1688 |         }
1689 | 
1690 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1691 |         return true
1692 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:2645:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2643 |         }
2644 |         if let textView = firstResponder as? NSTextView,
2645 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2646 |            field.accessibilityIdentifier() == identifier
2647 |         {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:10904:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10902 |         newName: String
10903 |     ) {
10904 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10905 |               let rename = current.rename,
10906 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14357:23: warning: no 'async' operations occur within 'await' expression
14355 |                 }
14356 | 
14357 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14358 |                     return
14359 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14370:35: warning: no 'async' operations occur within 'await' expression
14368 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14369 |                         && parse.reportsClipDirective
14370 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14371 |                         draft: draft,
14372 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14385:27: warning: no 'async' operations occur within 'await' expression
14383 |                     await completionGate.value
14384 |                     try Task.checkCancellation()
14385 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14386 |                         return
14387 |                     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14392:20: warning: no 'async' operations occur within 'await' expression
14390 |                 if let cursorUTF8Offset,
14391 |                    requestCompletion,
14392 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14393 |                        parse: parse,
14394 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14398:37: warning: no 'async' operations occur within 'await' expression
14396 |                    ) == true
14397 |                 {
14398 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14399 |                         parse: parse,
14400 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[242/252] Compiling BobMacCapture CaptureEditorTextConfiguration.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:1690:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1688 |         }
1689 | 
1690 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1691 |         return true
1692 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:2645:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2643 |         }
2644 |         if let textView = firstResponder as? NSTextView,
2645 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2646 |            field.accessibilityIdentifier() == identifier
2647 |         {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:10904:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10902 |         newName: String
10903 |     ) {
10904 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10905 |               let rename = current.rename,
10906 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14357:23: warning: no 'async' operations occur within 'await' expression
14355 |                 }
14356 | 
14357 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14358 |                     return
14359 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14370:35: warning: no 'async' operations occur within 'await' expression
14368 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14369 |                         && parse.reportsClipDirective
14370 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14371 |                         draft: draft,
14372 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14385:27: warning: no 'async' operations occur within 'await' expression
14383 |                     await completionGate.value
14384 |                     try Task.checkCancellation()
14385 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14386 |                         return
14387 |                     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14392:20: warning: no 'async' operations occur within 'await' expression
14390 |                 if let cursorUTF8Offset,
14391 |                    requestCompletion,
14392 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14393 |                        parse: parse,
14394 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14398:37: warning: no 'async' operations occur within 'await' expression
14396 |                    ) == true
14397 |                 {
14398 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14399 |                         parse: parse,
14400 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[243/252] Compiling BobMacCapture CaptureInboxRouteChoiceView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:1690:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1688 |         }
1689 | 
1690 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1691 |         return true
1692 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:2645:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2643 |         }
2644 |         if let textView = firstResponder as? NSTextView,
2645 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2646 |            field.accessibilityIdentifier() == identifier
2647 |         {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:10904:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10902 |         newName: String
10903 |     ) {
10904 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10905 |               let rename = current.rename,
10906 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14357:23: warning: no 'async' operations occur within 'await' expression
14355 |                 }
14356 | 
14357 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14358 |                     return
14359 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14370:35: warning: no 'async' operations occur within 'await' expression
14368 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14369 |                         && parse.reportsClipDirective
14370 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14371 |                         draft: draft,
14372 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14385:27: warning: no 'async' operations occur within 'await' expression
14383 |                     await completionGate.value
14384 |                     try Task.checkCancellation()
14385 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14386 |                         return
14387 |                     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14392:20: warning: no 'async' operations occur within 'await' expression
14390 |                 if let cursorUTF8Offset,
14391 |                    requestCompletion,
14392 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14393 |                        parse: parse,
14394 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14398:37: warning: no 'async' operations occur within 'await' expression
14396 |                    ) == true
14397 |                 {
14398 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14399 |                         parse: parse,
14400 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[244/252] Compiling BobMacCapture CaptureKeyCommandRouter.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:1690:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1688 |         }
1689 | 
1690 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1691 |         return true
1692 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:2645:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2643 |         }
2644 |         if let textView = firstResponder as? NSTextView,
2645 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2646 |            field.accessibilityIdentifier() == identifier
2647 |         {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:10904:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10902 |         newName: String
10903 |     ) {
10904 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10905 |               let rename = current.rename,
10906 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14357:23: warning: no 'async' operations occur within 'await' expression
14355 |                 }
14356 | 
14357 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14358 |                     return
14359 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14370:35: warning: no 'async' operations occur within 'await' expression
14368 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14369 |                         && parse.reportsClipDirective
14370 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14371 |                         draft: draft,
14372 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14385:27: warning: no 'async' operations occur within 'await' expression
14383 |                     await completionGate.value
14384 |                     try Task.checkCancellation()
14385 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14386 |                         return
14387 |                     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14392:20: warning: no 'async' operations occur within 'await' expression
14390 |                 if let cursorUTF8Offset,
14391 |                    requestCompletion,
14392 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14393 |                        parse: parse,
14394 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14398:37: warning: no 'async' operations occur within 'await' expression
14396 |                    ) == true
14397 |                 {
14398 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14399 |                         parse: parse,
14400 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[245/252] Compiling BobMacCapture CaptureListGroupCapsule.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:1690:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1688 |         }
1689 | 
1690 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1691 |         return true
1692 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:2645:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2643 |         }
2644 |         if let textView = firstResponder as? NSTextView,
2645 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2646 |            field.accessibilityIdentifier() == identifier
2647 |         {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:10904:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10902 |         newName: String
10903 |     ) {
10904 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10905 |               let rename = current.rename,
10906 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14357:23: warning: no 'async' operations occur within 'await' expression
14355 |                 }
14356 | 
14357 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14358 |                     return
14359 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14370:35: warning: no 'async' operations occur within 'await' expression
14368 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14369 |                         && parse.reportsClipDirective
14370 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14371 |                         draft: draft,
14372 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14385:27: warning: no 'async' operations occur within 'await' expression
14383 |                     await completionGate.value
14384 |                     try Task.checkCancellation()
14385 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14386 |                         return
14387 |                     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14392:20: warning: no 'async' operations occur within 'await' expression
14390 |                 if let cursorUTF8Offset,
14391 |                    requestCompletion,
14392 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14393 |                        parse: parse,
14394 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14398:37: warning: no 'async' operations occur within 'await' expression
14396 |                    ) == true
14397 |                 {
14398 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14399 |                         parse: parse,
14400 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[246/252] Compiling BobMacCapture CaptureMoveChoiceView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:1690:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1688 |         }
1689 | 
1690 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1691 |         return true
1692 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:2645:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2643 |         }
2644 |         if let textView = firstResponder as? NSTextView,
2645 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2646 |            field.accessibilityIdentifier() == identifier
2647 |         {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:10904:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10902 |         newName: String
10903 |     ) {
10904 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10905 |               let rename = current.rename,
10906 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14357:23: warning: no 'async' operations occur within 'await' expression
14355 |                 }
14356 | 
14357 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14358 |                     return
14359 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14370:35: warning: no 'async' operations occur within 'await' expression
14368 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14369 |                         && parse.reportsClipDirective
14370 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14371 |                         draft: draft,
14372 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14385:27: warning: no 'async' operations occur within 'await' expression
14383 |                     await completionGate.value
14384 |                     try Task.checkCancellation()
14385 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14386 |                         return
14387 |                     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14392:20: warning: no 'async' operations occur within 'await' expression
14390 |                 if let cursorUTF8Offset,
14391 |                    requestCompletion,
14392 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14393 |                        parse: parse,
14394 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14398:37: warning: no 'async' operations occur within 'await' expression
14396 |                    ) == true
14397 |                 {
14398 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14399 |                         parse: parse,
14400 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[247/252] Compiling BobMacCapture CapturePanelController.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:1690:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1688 |         }
1689 | 
1690 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1691 |         return true
1692 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:2645:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2643 |         }
2644 |         if let textView = firstResponder as? NSTextView,
2645 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2646 |            field.accessibilityIdentifier() == identifier
2647 |         {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:10904:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10902 |         newName: String
10903 |     ) {
10904 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10905 |               let rename = current.rename,
10906 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14357:23: warning: no 'async' operations occur within 'await' expression
14355 |                 }
14356 | 
14357 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14358 |                     return
14359 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14370:35: warning: no 'async' operations occur within 'await' expression
14368 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14369 |                         && parse.reportsClipDirective
14370 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14371 |                         draft: draft,
14372 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14385:27: warning: no 'async' operations occur within 'await' expression
14383 |                     await completionGate.value
14384 |                     try Task.checkCancellation()
14385 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14386 |                         return
14387 |                     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14392:20: warning: no 'async' operations occur within 'await' expression
14390 |                 if let cursorUTF8Offset,
14391 |                    requestCompletion,
14392 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14393 |                        parse: parse,
14394 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14398:37: warning: no 'async' operations occur within 'await' expression
14396 |                    ) == true
14397 |                 {
14398 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14399 |                         parse: parse,
14400 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[248/252] Compiling BobMacCapture CapturePanelModel.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:1690:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1688 |         }
1689 | 
1690 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1691 |         return true
1692 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:2645:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2643 |         }
2644 |         if let textView = firstResponder as? NSTextView,
2645 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2646 |            field.accessibilityIdentifier() == identifier
2647 |         {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:10904:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10902 |         newName: String
10903 |     ) {
10904 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10905 |               let rename = current.rename,
10906 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14357:23: warning: no 'async' operations occur within 'await' expression
14355 |                 }
14356 | 
14357 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14358 |                     return
14359 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14370:35: warning: no 'async' operations occur within 'await' expression
14368 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14369 |                         && parse.reportsClipDirective
14370 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14371 |                         draft: draft,
14372 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14385:27: warning: no 'async' operations occur within 'await' expression
14383 |                     await completionGate.value
14384 |                     try Task.checkCancellation()
14385 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14386 |                         return
14387 |                     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14392:20: warning: no 'async' operations occur within 'await' expression
14390 |                 if let cursorUTF8Offset,
14391 |                    requestCompletion,
14392 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14393 |                        parse: parse,
14394 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14398:37: warning: no 'async' operations occur within 'await' expression
14396 |                    ) == true
14397 |                 {
14398 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14399 |                         parse: parse,
14400 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[249/252] Compiling BobMacCapture CapturePanelView.swift
/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:1690:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1688 |         }
1689 | 
1690 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1691 |         return true
1692 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelController.swift:2645:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2643 |         }
2644 |         if let textView = firstResponder as? NSTextView,
2645 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2646 |            field.accessibilityIdentifier() == identifier
2647 |         {

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:3095:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3093 |                         requireInboxRouteChoice: true,
 3094 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 3095 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 3096 |                     )
 3097 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:10904:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10902 |         newName: String
10903 |     ) {
10904 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10905 |               let rename = current.rename,
10906 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14357:23: warning: no 'async' operations occur within 'await' expression
14355 |                 }
14356 | 
14357 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14358 |                     return
14359 |                 }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14370:35: warning: no 'async' operations occur within 'await' expression
14368 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14369 |                         && parse.reportsClipDirective
14370 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14371 |                         draft: draft,
14372 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14385:27: warning: no 'async' operations occur within 'await' expression
14383 |                     await completionGate.value
14384 |                     try Task.checkCancellation()
14385 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14386 |                         return
14387 |                     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14392:20: warning: no 'async' operations occur within 'await' expression
14390 |                 if let cursorUTF8Offset,
14391 |                    requestCompletion,
14392 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14393 |                        parse: parse,
14394 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelModel.swift:14398:37: warning: no 'async' operations occur within 'await' expression
14396 |                    ) == true
14397 |                 {
14398 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14399 |                         parse: parse,
14400 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-flip/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[249/252] Write Objects.LinkFileList
[250/252] Linking BobMacCapture
[251/252] Applying BobMacCapture
Build complete! (104.93s)
PASS BobMacCaptureTests
PASS BobMacCaptureInstallHelperTests
PASS CaptureCoreTests
PASS RefsCoreTests
Type-check only: macOS test targets were checked against a stub; CI still runs the tests.
succeeded  exit=0  duration=339811ms

