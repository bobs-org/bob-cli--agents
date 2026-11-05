# Chat History - ace-run (bob-cli-h4.4--mon)

- **TIMESTAMP:** 2026-11-05 06:46:56 EST
- **MODEL:** codex/gpt-6-astra
- **AGENT:** bob-cli-h4.4--mon

## Prompt

sase monitor start --command 'python3 .git/h4-verification/verify-mac.py' --reason 'Complete bob-cli-h4.4 pending macOS scratch release bundle and test type-check'

## Response

sase tool run 0f50a830cb5932e03436fdb154da0585
Verifying linked checkout: c95094da4e7b743ebd7f2a8dc36262777da8efdd
Remote scratch: /private/tmp/bob-cli-h4.4-verify.evdb7uQZ
Building for production...
[0/6] Write sources
[3/6] Write swift-version--1AB21518FC5DEDBE.txt
[5/7] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9270:13: warning: no calls to throwing functions occur within 'try' expression
 9268 |         let container = try decoder.singleValueContainer()
 9269 |         // Explicit null has no value; treat it as absent.
 9270 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9271 |             throw DecodingError.valueNotFound(
 9272 |                 CaptureThemeSuggestion.self,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[6/8] Compiling RefsCore HighlightsSaveScan.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:1634:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1632 |         }
1633 | 
1634 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1635 |         return true
1636 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:2461:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2459 |         }
2460 |         if let textView = firstResponder as? NSTextView,
2461 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2462 |            field.accessibilityIdentifier() == identifier
2463 |         {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:10691:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10689 |         newName: String
10690 |     ) {
10691 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10692 |               let rename = current.rename,
10693 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14082:23: warning: no 'async' operations occur within 'await' expression
14080 |                 }
14081 | 
14082 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14083 |                     return
14084 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14095:35: warning: no 'async' operations occur within 'await' expression
14093 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14094 |                         && parse.reportsClipDirective
14095 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14096 |                         draft: draft,
14097 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14110:27: warning: no 'async' operations occur within 'await' expression
14108 |                     await completionGate.value
14109 |                     try Task.checkCancellation()
14110 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14111 |                         return
14112 |                     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14117:20: warning: no 'async' operations occur within 'await' expression
14115 |                 if let cursorUTF8Offset,
14116 |                    requestCompletion,
14117 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14118 |                        parse: parse,
14119 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14123:37: warning: no 'async' operations occur within 'await' expression
14121 |                    ) == true
14122 |                 {
14123 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14124 |                         parse: parse,
14125 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
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
Build of product 'BobMacCapture' complete! (242.06s)
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/.build/bundle/Bob Mac Capture.app/Contents/MacOS/BobMacCapture: replacing existing signature
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/.build/bundle/Bob Mac Capture.app: replacing existing signature
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/.build/bundle/Bob Mac Capture.app
./Scripts/typecheck-tests.sh
Building for debugging...
[0/18] Write sources
[5/18] Write BobMacCapture-entitlement.plist
[5/18] Write refs-rank-entitlement.plist
[5/18] Write BobMacCaptureInstallHelper-entitlement.plist
[8/18] Write swift-version--1AB21518FC5DEDBE.txt
[10/103] Compiling CaptureCore CapturePomodoroPastPresentation.swift
[11/103] Compiling CaptureCore CapturePomodoroResetPresentation.swift
[12/103] Compiling CaptureCore CapturePomodoroShiftPresentation.swift
[13/103] Compiling CaptureCore CapturePomodoroSplitPresentation.swift
[14/103] Compiling CaptureCore CapturePomodoroStartPresentation.swift
[15/103] Compiling CaptureCore CaptureProjectNotePresentation.swift
[16/103] Compiling CaptureCore CaptureRefFileUnder.swift
[17/103] Compiling CaptureCore CaptureRefPresentation.swift
[18/103] Compiling CaptureCore CaptureRelatedModels.swift
[19/103] Compiling CaptureCore CaptureRelationCancelPresentation.swift
[20/103] Compiling CaptureCore CaptureRelationCloseEffect.swift
[21/103] Compiling CaptureCore CaptureRelationCompletePresentation.swift
[22/103] Compiling CaptureCore CaptureOpenPlan.swift
[23/103] Compiling CaptureCore CapturePanelPlacement.swift
[24/103] Compiling CaptureCore CapturePastBoundary.swift
[25/103] Compiling CaptureCore CapturePickerHelpers.swift
[26/103] Compiling CaptureCore CapturePickerPresentation.swift
[27/103] Compiling CaptureCore CapturePlanBudgetPresentation.swift
[28/103] Compiling CaptureCore CapturePomodoroAdjustPresentation.swift
[29/103] Compiling CaptureCore CapturePomodoroBlockPresentation.swift
[30/103] Compiling CaptureCore CapturePomodoroClosePresentation.swift
[31/103] Compiling CaptureCore CapturePomodoroLineTokens.swift
[32/103] Compiling CaptureCore CapturePomodoroLinkPresentation.swift
[33/103] Compiling CaptureCore CapturePomodoroMergePresentation.swift
[34/103] Compiling CaptureCore CaptureTaskThemePresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[35/103] Compiling CaptureCore CaptureTaskTypeMenuPresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[36/103] Compiling CaptureCore CaptureTextRanges.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[37/103] Compiling CaptureCore CaptureTodayPomodoroGoto.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[38/103] Compiling CaptureCore CaptureTogglePresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[39/103] Compiling CaptureCore CaptureTransferPresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[40/103] Compiling CaptureCore CaptureUnconfiguredThemePresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[41/103] Compiling CaptureCore CaptureWordMotion.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[42/103] Compiling CaptureCore CompletionRowContent.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[43/103] Compiling CaptureCore DependencyPickerPresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[44/103] Compiling CaptureCore FuzzyMatcher.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[45/103] Compiling CaptureCore ObsidianOpenURL.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[46/114] Compiling CaptureCore CaptureRelationHeldPresentation.swift
[47/114] Compiling CaptureCore CaptureRelationSuccessorModels.swift
[48/114] Compiling CaptureCore CaptureRelationshipCopy.swift
[49/114] Compiling CaptureCore CaptureRelationshipPresentation.swift
[50/114] Compiling CaptureCore CaptureSavedTemplates.swift
[51/114] Compiling CaptureCore CaptureSubBulletPresentation.swift
[52/114] Compiling CaptureCore CaptureSuccessorOfferRows.swift
[53/114] Compiling CaptureCore CaptureSuccessorPresentation.swift
[54/114] Compiling CaptureCore CaptureTargetsCache.swift
[55/114] Compiling CaptureCore CaptureTaskBlockPresentation.swift
[56/114] Compiling CaptureCore CaptureTaskCompletePresentation.swift
[57/114] Compiling CaptureCore CaptureTaskGotoScopeState.swift
[58/114] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[59/114] Compiling CaptureCore BlockIDPickerIndex.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[60/114] Compiling CaptureCore BlockIDRules.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[61/114] Compiling CaptureCore BobEnvironment.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[62/114] Compiling CaptureCore BobErrors.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[63/114] Compiling CaptureCore BobExecutableResolver.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[64/114] Compiling CaptureCore BobMacCaptureLaunchContext.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[65/114] Compiling CaptureCore BobProcessClient.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[66/114] Compiling CaptureCore CanceledDraftStashStore.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[67/114] Compiling CaptureCore CaptureAgendaBoundaryRefresh.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[68/114] Compiling CaptureCore CaptureAgendaFitPlanner.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[69/114] Compiling CaptureCore CaptureAgendaHold.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[70/114] Compiling CaptureCore CaptureAgendaInlineText.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[71/114] Compiling CaptureCore CaptureAgendaLayout.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[72/114] Compiling CaptureCore CaptureAgendaModels.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[73/114] Compiling CaptureCore CaptureAgendaPresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[74/114] Compiling CaptureCore CaptureAgendaRefreshFilter.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[75/114] Compiling CaptureCore CaptureAgendaRefreshState.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[76/114] Compiling CaptureCore CaptureAgendaVisibility.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[77/114] Compiling CaptureCore CaptureBlockDiffRow.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[78/114] Compiling CaptureCore CaptureBlockIDSplice.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[79/114] Compiling CaptureCore CaptureClipPresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[80/114] Compiling CaptureCore CaptureCloseTaskCommaAssist.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[81/114] Compiling CaptureCore CaptureCloseTaskCommaProvenance.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[82/114] Emitting module CaptureCore
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[83/114] Compiling CaptureCore ParentTaskPickerPresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[84/114] Compiling CaptureCore PomodoroHomes.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[85/114] Compiling CaptureCore ProjectTaskMovePickerPresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[86/114] Compiling CaptureCore SimilarTasksBandEdits.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[87/114] Compiling CaptureCore SimilarTasksBandPolicy.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[88/114] Compiling CaptureCore SimilarTasksBandPresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[89/114] Compiling CaptureCore TaskCompletePickerPresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[90/114] Compiling CaptureCore TaskDisplayText.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[91/114] Compiling CaptureCore TaskLinkPickerPresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[92/114] Compiling CaptureCore WikilinkTaskPickerPresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[93/114] Compiling CaptureCore WorkBadgeTone.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ParentTaskPickerPresentation.swift:612:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
610 | 
611 | private struct ParentTaskPickerIndexEntry: Sendable {
612 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
613 |     let bobIndex: Int
614 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/TaskLinkPickerPresentation.swift:532:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
530 | /// searchable.
531 | private struct TaskLinkPickerIndexEntry: Sendable {
532 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
533 |     let bobIndex: Int
534 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9471:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9469 | }
 9470 | 
 9471 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9472 |     public let replacement: String
 9473 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[94/114] Compiling CaptureCore CaptureCompletionMenu.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9270:13: warning: no calls to throwing functions occur within 'try' expression
 9268 |         let container = try decoder.singleValueContainer()
 9269 |         // Explicit null has no value; treat it as absent.
 9270 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9271 |             throw DecodingError.valueNotFound(
 9272 |                 CaptureThemeSuggestion.self,
[95/114] Compiling CaptureCore CaptureDrawerMenuPresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9270:13: warning: no calls to throwing functions occur within 'try' expression
 9268 |         let container = try decoder.singleValueContainer()
 9269 |         // Explicit null has no value; treat it as absent.
 9270 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9271 |             throw DecodingError.valueNotFound(
 9272 |                 CaptureThemeSuggestion.self,
[96/114] Compiling CaptureCore CaptureEditWrite.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9270:13: warning: no calls to throwing functions occur within 'try' expression
 9268 |         let container = try decoder.singleValueContainer()
 9269 |         // Explicit null has no value; treat it as absent.
 9270 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9271 |             throw DecodingError.valueNotFound(
 9272 |                 CaptureThemeSuggestion.self,
[97/114] Compiling CaptureCore CaptureGrammarGate.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9270:13: warning: no calls to throwing functions occur within 'try' expression
 9268 |         let container = try decoder.singleValueContainer()
 9269 |         // Explicit null has no value; treat it as absent.
 9270 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9271 |             throw DecodingError.valueNotFound(
 9272 |                 CaptureThemeSuggestion.self,
[98/114] Compiling CaptureCore CaptureInboxRoutePresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9270:13: warning: no calls to throwing functions occur within 'try' expression
 9268 |         let container = try decoder.singleValueContainer()
 9269 |         // Explicit null has no value; treat it as absent.
 9270 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9271 |             throw DecodingError.valueNotFound(
 9272 |                 CaptureThemeSuggestion.self,
[99/114] Compiling CaptureCore CaptureLineCaseToggle.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9270:13: warning: no calls to throwing functions occur within 'try' expression
 9268 |         let container = try decoder.singleValueContainer()
 9269 |         // Explicit null has no value; treat it as absent.
 9270 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9271 |             throw DecodingError.valueNotFound(
 9272 |                 CaptureThemeSuggestion.self,
[100/114] Compiling CaptureCore CaptureLinkGuardPresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9270:13: warning: no calls to throwing functions occur within 'try' expression
 9268 |         let container = try decoder.singleValueContainer()
 9269 |         // Explicit null has no value; treat it as absent.
 9270 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9271 |             throw DecodingError.valueNotFound(
 9272 |                 CaptureThemeSuggestion.self,
[101/114] Compiling CaptureCore CaptureList.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9270:13: warning: no calls to throwing functions occur within 'try' expression
 9268 |         let container = try decoder.singleValueContainer()
 9269 |         // Explicit null has no value; treat it as absent.
 9270 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9271 |             throw DecodingError.valueNotFound(
 9272 |                 CaptureThemeSuggestion.self,
[102/114] Compiling CaptureCore CaptureModels.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9270:13: warning: no calls to throwing functions occur within 'try' expression
 9268 |         let container = try decoder.singleValueContainer()
 9269 |         // Explicit null has no value; treat it as absent.
 9270 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9271 |             throw DecodingError.valueNotFound(
 9272 |                 CaptureThemeSuggestion.self,
[103/114] Compiling CaptureCore CaptureMoveChoicePresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9270:13: warning: no calls to throwing functions occur within 'try' expression
 9268 |         let container = try decoder.singleValueContainer()
 9269 |         // Explicit null has no value; treat it as absent.
 9270 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9271 |             throw DecodingError.valueNotFound(
 9272 |                 CaptureThemeSuggestion.self,
[104/114] Compiling CaptureCore CaptureNotePullPresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9270:13: warning: no calls to throwing functions occur within 'try' expression
 9268 |         let container = try decoder.singleValueContainer()
 9269 |         // Explicit null has no value; treat it as absent.
 9270 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9271 |             throw DecodingError.valueNotFound(
 9272 |                 CaptureThemeSuggestion.self,
[105/114] Compiling CaptureCore CaptureOpenHintPresentation.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/CaptureCore/CaptureModels.swift:9270:13: warning: no calls to throwing functions occur within 'try' expression
 9268 |         let container = try decoder.singleValueContainer()
 9269 |         // Explicit null has no value; treat it as absent.
 9270 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 9271 |             throw DecodingError.valueNotFound(
 9272 |                 CaptureThemeSuggestion.self,
[106/150] Compiling RefsCore RefsNew.swift
[107/150] Compiling RefsCore RefsNewest.swift
[108/150] Compiling RefsCore RefsPDFUpdates.swift
[109/150] Compiling RefsCore RefsPanelGeometry.swift
[110/154] Compiling RefsCore RefsScan.swift
[111/154] Compiling RefsCore RefsScanReceipt.swift
[112/154] Compiling RefsCore RefsSectionedWindow.swift
[113/154] Compiling RefsCore RefsSelection.swift
[114/154] Emitting module RefsCore
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[115/154] Compiling RefsCore RefsPickerScope.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[116/154] Compiling RefsCore RefsQuoteUnderline.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[117/154] Compiling RefsCore RefsRanking.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[118/154] Compiling RefsCore RefsRename.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[119/154] Compiling RefsCore RefsDecoding.swift
[120/154] Compiling RefsCore RefsFetching.swift
[121/154] Compiling RefsCore RefsHighlightPicker.swift
[122/154] Compiling RefsCore RefsHighlightsTabs.swift
[123/154] Compiling RefsCore RefsInspector.swift
[124/154] Compiling RefsCore RefsInspectorImages.swift
[125/154] Compiling RefsCore RefsLinks.swift
[126/154] Compiling RefsCore RefsListScroll.swift
[127/154] Compiling RefsCore RefsModel.swift
[128/154] Compiling RefsCore HighlightsSaveScan.swift
[129/154] Compiling RefsCore RefsArrivals.swift
[130/154] Compiling RefsCore RefsCaption.swift
[131/154] Compiling RefsCore RefsCode.swift
[132/154] Compiling RefsCore RefsCopy.swift
[133/154] Compiling RefsCore RefsStores.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[134/154] Compiling RefsCore RefsTabClose.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[135/154] Compiling RefsCore RefsTabsRanking.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[136/154] Compiling RefsCore RefsToday.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[137/154] Compiling RefsCore RefsTodayLinkCard.swift
[138/154] Compiling RefsCore RefsTodayLinkModels.swift
[139/154] Compiling RefsCore RefsTodayLinkPresentation.swift
[140/154] Compiling RefsCore RefsWatcherRelevance.swift
[141/238] Emitting module refs_rank
[142/238] Compiling refs_rank main.swift
[142/238] Write Objects.LinkFileList
[143/238] Linking refs-rank
[144/238] Applying refs-rank
[146/238] Emitting module BobMacCaptureInstallHelper
[147/238] Compiling BobMacCaptureInstallHelper BobMacCaptureInstallHelperMain.swift
[148/238] Compiling BobMacCaptureInstallHelper InstallHelperError.swift
[149/238] Compiling BobMacCaptureInstallHelper InstallHelperArguments.swift
[150/238] Compiling BobMacCaptureInstallHelper InstallRelauncher.swift
[150/238] Write Objects.LinkFileList
[151/238] Linking BobMacCaptureInstallHelper
[152/238] Applying BobMacCaptureInstallHelper
[154/238] Emitting module BobMacCapture
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[155/249] Compiling BobMacCapture AccessibilityTrust.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[156/249] Compiling BobMacCapture AppDelegate.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[157/249] Compiling BobMacCapture AppRelauncher.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[158/249] Compiling BobMacCapture AppSettings.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[159/249] Compiling BobMacCapture BlockDiffCard.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[160/249] Compiling BobMacCapture BlockIDField.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[161/249] Compiling BobMacCapture BobMacCaptureMain.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[162/249] Compiling BobMacCapture BobPanelCoordinator.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[163/249] Compiling BobMacCapture BundleSigningInspector.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[164/249] Compiling BobMacCapture CanceledDraftStash.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[165/249] Compiling BobMacCapture CaptureAgendaRowMeasurer.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[166/249] Compiling BobMacCapture CaptureAgendaStore.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[167/249] Compiling BobMacCapture RefsSearchBar.swift
[168/249] Compiling BobMacCapture RefsTabsViews.swift
[169/249] Compiling BobMacCapture RefsTodayLinkCardView.swift
[170/249] Compiling BobMacCapture RefsUnderlineRenderer.swift
[171/249] Compiling BobMacCapture RefsVisualTokens.swift
[172/249] Compiling BobMacCapture RefsAliasHotkeyRegistration.swift
[173/249] Compiling BobMacCapture RefsHighlightsCodeKey.swift
[174/249] Compiling BobMacCapture RefsHighlightsCopyKey.swift
[175/249] Compiling BobMacCapture RefsHighlightsLinkKey.swift
[176/249] Compiling BobMacCapture RefsHighlightsOpenKey.swift
[177/249] Compiling BobMacCapture RefsHighlightsTabsKey.swift
[178/249] Compiling BobMacCapture RefsHotkeyRegistration.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[179/249] Compiling BobMacCapture RelationLabelField.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[180/249] Compiling BobMacCapture SavedTemplateShelf.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[181/249] Compiling BobMacCapture SettingsView.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[182/249] Compiling BobMacCapture Signposts.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[183/249] Compiling BobMacCapture SimilarTasksBandView.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[184/249] Compiling BobMacCapture StatusItemController.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[185/249] Compiling BobMacCapture StatusItemGlyph.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[186/249] Compiling BobMacCapture TaskBlockView.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[187/249] Compiling BobMacCapture TodayBadge.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[188/249] Compiling BobMacCapture VaultTargetWatcher.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[189/249] Compiling BobMacCapture RefsAnnotationImages.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[190/249] Compiling BobMacCapture RefsCodePreviewWell.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[191/249] Compiling BobMacCapture RefsCopyCardView.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[192/249] Compiling BobMacCapture RefsCopyHUD.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[193/249] Compiling BobMacCapture RefsFooter.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[194/249] Compiling BobMacCapture RefsInspectorImageViews.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[195/249] Compiling BobMacCapture RefsInspectorLoader.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[196/249] Compiling BobMacCapture RefsInspectorScroll.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[197/249] Compiling BobMacCapture RefsInspectorView.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[198/249] Compiling BobMacCapture RefsKeyRouter.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[199/249] Compiling BobMacCapture RefsLibrary.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:771:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
 771 |             + Text(String(row.preview[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 772 |                 .foregroundStyle(.secondary)
 773 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:770:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 768 |         return Text(String(row.preview[..<range.lowerBound]))
 769 |             .foregroundStyle(.secondary)
 770 |             + Text("●").foregroundStyle(Color.accentColor)
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 771 |             + Text(String(row.preview[range.upperBound...]))
 772 |                 .foregroundStyle(.secondary)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[200/249] Compiling BobMacCapture CapturePanelWindowSizer.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[201/249] Compiling BobMacCapture CapturePickerFilterField.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[202/249] Compiling BobMacCapture CapturePickerState.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[203/249] Compiling BobMacCapture CapturePickerView.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[204/249] Compiling BobMacCapture CapturePlanBudgetMeterRow.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[205/249] Compiling BobMacCapture CapturePullInChoice.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[206/249] Compiling BobMacCapture CapturePullInChoiceView.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[207/249] Compiling BobMacCapture CaptureShowRefreshWindow.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[208/249] Compiling BobMacCapture CaptureSnippetResolver.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[209/249] Compiling BobMacCapture CaptureTargetsRefreshGate.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[210/249] Compiling BobMacCapture CaptureTaskTypeMenuView.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[211/249] Compiling BobMacCapture CaptureTransferCardView.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePullInChoiceView.swift:768:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
766 |             let chunk = Text("\(separator)\(entry.element.text)")
767 |                 .foregroundStyle(entry.element.tint ?? .secondary)
768 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
769 |         }
770 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[212/249] Compiling BobMacCapture ClipCardView.swift
[213/249] Compiling BobMacCapture HighlightsSaveKeyMonitor.swift
[214/249] Compiling BobMacCapture HighlightsTakeover.swift
[215/249] Compiling BobMacCapture HotKeyRegistry.swift
[216/249] Compiling BobMacCapture NotificationService.swift
[217/249] Compiling BobMacCapture PlainTextPaste.swift
[218/249] Compiling BobMacCapture PomodoroBlockView.swift
[219/249] Compiling BobMacCapture PomodoroHomeColor.swift
[220/249] Compiling BobMacCapture PomodoroNameField.swift
[221/249] Compiling BobMacCapture PomodoroThemeViews.swift
[222/249] Compiling BobMacCapture AXHighlightsTabsReader.swift
[223/249] Compiling BobMacCapture RefsActionsMenu.swift
[224/249] Compiling BobMacCapture RefsLinkPreviewWell.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[225/249] Compiling BobMacCapture RefsListView.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[226/249] Compiling BobMacCapture RefsPanel.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[227/249] Compiling BobMacCapture RefsPanelModel.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[228/249] Compiling BobMacCapture RefsPanelStates.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[229/249] Compiling BobMacCapture RefsPanelView.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[230/249] Compiling BobMacCapture RefsPickerScopeViews.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[231/249] Compiling BobMacCapture RefsQuoteText.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[232/249] Compiling BobMacCapture RefsRenameCardView.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[233/249] Compiling BobMacCapture RefsRowView.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[234/249] Compiling BobMacCapture RefsScanReceiptObserver.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:811:20: warning: no 'async' operations occur within 'await' expression
 809 |         }.store(in: &subscriptions)
 810 |         library.$refreshState.sink { [weak self] _ in
 811 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 812 |         }.store(in: &subscriptions)
 813 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3281:21: warning: no 'async' operations occur within 'await' expression
3279 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3280 |                 Task {
3281 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3282 |                 }
3283 |             }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3710:13: warning: result of call to 'openSelected' is unused [#no-usage]
3708 |             openWithDefaultApp(item)
3709 |         case .note, .reveal, .task:
3710 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3711 |         }
3712 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3747:17: warning: no 'async' operations occur within 'await' expression
3745 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3746 |             Task {
3747 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3748 |             }
3749 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3774:17: warning: no 'async' operations occur within 'await' expression
3772 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3773 |             Task {
3774 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3775 |             }
3776 |         }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3843:17: warning: no 'async' operations occur within 'await' expression
3841 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3842 |             Task {
3843 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3844 |                     itemID: item.id,
3845 |                     title: item.title.text,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3874:17: warning: no 'async' operations occur within 'await' expression
3872 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3873 |             Task {
3874 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3875 |                     itemID: item.id,
3876 |                     title: item.title.text,
[235/249] Compiling BobMacCapture CaptureAgendaView.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:1634:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1632 |         }
1633 | 
1634 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1635 |         return true
1636 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:2461:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2459 |         }
2460 |         if let textView = firstResponder as? NSTextView,
2461 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2462 |            field.accessibilityIdentifier() == identifier
2463 |         {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:10691:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10689 |         newName: String
10690 |     ) {
10691 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10692 |               let rename = current.rename,
10693 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14082:23: warning: no 'async' operations occur within 'await' expression
14080 |                 }
14081 | 
14082 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14083 |                     return
14084 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14095:35: warning: no 'async' operations occur within 'await' expression
14093 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14094 |                         && parse.reportsClipDirective
14095 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14096 |                         draft: draft,
14097 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14110:27: warning: no 'async' operations occur within 'await' expression
14108 |                     await completionGate.value
14109 |                     try Task.checkCancellation()
14110 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14111 |                         return
14112 |                     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14117:20: warning: no 'async' operations occur within 'await' expression
14115 |                 if let cursorUTF8Offset,
14116 |                    requestCompletion,
14117 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14118 |                        parse: parse,
14119 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14123:37: warning: no 'async' operations occur within 'await' expression
14121 |                    ) == true
14122 |                 {
14123 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14124 |                         parse: parse,
14125 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[236/249] Compiling BobMacCapture CaptureAliasHotkeyRegistration.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:1634:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1632 |         }
1633 | 
1634 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1635 |         return true
1636 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:2461:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2459 |         }
2460 |         if let textView = firstResponder as? NSTextView,
2461 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2462 |            field.accessibilityIdentifier() == identifier
2463 |         {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:10691:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10689 |         newName: String
10690 |     ) {
10691 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10692 |               let rename = current.rename,
10693 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14082:23: warning: no 'async' operations occur within 'await' expression
14080 |                 }
14081 | 
14082 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14083 |                     return
14084 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14095:35: warning: no 'async' operations occur within 'await' expression
14093 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14094 |                         && parse.reportsClipDirective
14095 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14096 |                         draft: draft,
14097 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14110:27: warning: no 'async' operations occur within 'await' expression
14108 |                     await completionGate.value
14109 |                     try Task.checkCancellation()
14110 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14111 |                         return
14112 |                     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14117:20: warning: no 'async' operations occur within 'await' expression
14115 |                 if let cursorUTF8Offset,
14116 |                    requestCompletion,
14117 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14118 |                        parse: parse,
14119 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14123:37: warning: no 'async' operations occur within 'await' expression
14121 |                    ) == true
14122 |                 {
14123 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14124 |                         parse: parse,
14125 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[237/249] Compiling BobMacCapture CaptureDrawerMenuView.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:1634:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1632 |         }
1633 | 
1634 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1635 |         return true
1636 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:2461:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2459 |         }
2460 |         if let textView = firstResponder as? NSTextView,
2461 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2462 |            field.accessibilityIdentifier() == identifier
2463 |         {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:10691:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10689 |         newName: String
10690 |     ) {
10691 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10692 |               let rename = current.rename,
10693 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14082:23: warning: no 'async' operations occur within 'await' expression
14080 |                 }
14081 | 
14082 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14083 |                     return
14084 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14095:35: warning: no 'async' operations occur within 'await' expression
14093 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14094 |                         && parse.reportsClipDirective
14095 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14096 |                         draft: draft,
14097 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14110:27: warning: no 'async' operations occur within 'await' expression
14108 |                     await completionGate.value
14109 |                     try Task.checkCancellation()
14110 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14111 |                         return
14112 |                     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14117:20: warning: no 'async' operations occur within 'await' expression
14115 |                 if let cursorUTF8Offset,
14116 |                    requestCompletion,
14117 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14118 |                        parse: parse,
14119 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14123:37: warning: no 'async' operations occur within 'await' expression
14121 |                    ) == true
14122 |                 {
14123 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14124 |                         parse: parse,
14125 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[238/249] Compiling BobMacCapture CaptureEditorPalette.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:1634:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1632 |         }
1633 | 
1634 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1635 |         return true
1636 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:2461:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2459 |         }
2460 |         if let textView = firstResponder as? NSTextView,
2461 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2462 |            field.accessibilityIdentifier() == identifier
2463 |         {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:10691:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10689 |         newName: String
10690 |     ) {
10691 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10692 |               let rename = current.rename,
10693 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14082:23: warning: no 'async' operations occur within 'await' expression
14080 |                 }
14081 | 
14082 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14083 |                     return
14084 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14095:35: warning: no 'async' operations occur within 'await' expression
14093 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14094 |                         && parse.reportsClipDirective
14095 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14096 |                         draft: draft,
14097 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14110:27: warning: no 'async' operations occur within 'await' expression
14108 |                     await completionGate.value
14109 |                     try Task.checkCancellation()
14110 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14111 |                         return
14112 |                     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14117:20: warning: no 'async' operations occur within 'await' expression
14115 |                 if let cursorUTF8Offset,
14116 |                    requestCompletion,
14117 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14118 |                        parse: parse,
14119 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14123:37: warning: no 'async' operations occur within 'await' expression
14121 |                    ) == true
14122 |                 {
14123 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14124 |                         parse: parse,
14125 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[239/249] Compiling BobMacCapture CaptureEditorTextConfiguration.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:1634:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1632 |         }
1633 | 
1634 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1635 |         return true
1636 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:2461:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2459 |         }
2460 |         if let textView = firstResponder as? NSTextView,
2461 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2462 |            field.accessibilityIdentifier() == identifier
2463 |         {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:10691:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10689 |         newName: String
10690 |     ) {
10691 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10692 |               let rename = current.rename,
10693 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14082:23: warning: no 'async' operations occur within 'await' expression
14080 |                 }
14081 | 
14082 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14083 |                     return
14084 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14095:35: warning: no 'async' operations occur within 'await' expression
14093 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14094 |                         && parse.reportsClipDirective
14095 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14096 |                         draft: draft,
14097 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14110:27: warning: no 'async' operations occur within 'await' expression
14108 |                     await completionGate.value
14109 |                     try Task.checkCancellation()
14110 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14111 |                         return
14112 |                     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14117:20: warning: no 'async' operations occur within 'await' expression
14115 |                 if let cursorUTF8Offset,
14116 |                    requestCompletion,
14117 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14118 |                        parse: parse,
14119 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14123:37: warning: no 'async' operations occur within 'await' expression
14121 |                    ) == true
14122 |                 {
14123 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14124 |                         parse: parse,
14125 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[240/249] Compiling BobMacCapture CaptureInboxRouteChoiceView.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:1634:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1632 |         }
1633 | 
1634 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1635 |         return true
1636 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:2461:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2459 |         }
2460 |         if let textView = firstResponder as? NSTextView,
2461 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2462 |            field.accessibilityIdentifier() == identifier
2463 |         {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:10691:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10689 |         newName: String
10690 |     ) {
10691 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10692 |               let rename = current.rename,
10693 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14082:23: warning: no 'async' operations occur within 'await' expression
14080 |                 }
14081 | 
14082 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14083 |                     return
14084 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14095:35: warning: no 'async' operations occur within 'await' expression
14093 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14094 |                         && parse.reportsClipDirective
14095 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14096 |                         draft: draft,
14097 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14110:27: warning: no 'async' operations occur within 'await' expression
14108 |                     await completionGate.value
14109 |                     try Task.checkCancellation()
14110 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14111 |                         return
14112 |                     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14117:20: warning: no 'async' operations occur within 'await' expression
14115 |                 if let cursorUTF8Offset,
14116 |                    requestCompletion,
14117 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14118 |                        parse: parse,
14119 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14123:37: warning: no 'async' operations occur within 'await' expression
14121 |                    ) == true
14122 |                 {
14123 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14124 |                         parse: parse,
14125 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[241/249] Compiling BobMacCapture CaptureKeyCommandRouter.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:1634:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1632 |         }
1633 | 
1634 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1635 |         return true
1636 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:2461:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2459 |         }
2460 |         if let textView = firstResponder as? NSTextView,
2461 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2462 |            field.accessibilityIdentifier() == identifier
2463 |         {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:10691:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10689 |         newName: String
10690 |     ) {
10691 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10692 |               let rename = current.rename,
10693 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14082:23: warning: no 'async' operations occur within 'await' expression
14080 |                 }
14081 | 
14082 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14083 |                     return
14084 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14095:35: warning: no 'async' operations occur within 'await' expression
14093 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14094 |                         && parse.reportsClipDirective
14095 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14096 |                         draft: draft,
14097 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14110:27: warning: no 'async' operations occur within 'await' expression
14108 |                     await completionGate.value
14109 |                     try Task.checkCancellation()
14110 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14111 |                         return
14112 |                     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14117:20: warning: no 'async' operations occur within 'await' expression
14115 |                 if let cursorUTF8Offset,
14116 |                    requestCompletion,
14117 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14118 |                        parse: parse,
14119 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14123:37: warning: no 'async' operations occur within 'await' expression
14121 |                    ) == true
14122 |                 {
14123 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14124 |                         parse: parse,
14125 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[242/249] Compiling BobMacCapture CaptureListGroupCapsule.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:1634:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1632 |         }
1633 | 
1634 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1635 |         return true
1636 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:2461:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2459 |         }
2460 |         if let textView = firstResponder as? NSTextView,
2461 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2462 |            field.accessibilityIdentifier() == identifier
2463 |         {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:10691:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10689 |         newName: String
10690 |     ) {
10691 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10692 |               let rename = current.rename,
10693 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14082:23: warning: no 'async' operations occur within 'await' expression
14080 |                 }
14081 | 
14082 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14083 |                     return
14084 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14095:35: warning: no 'async' operations occur within 'await' expression
14093 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14094 |                         && parse.reportsClipDirective
14095 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14096 |                         draft: draft,
14097 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14110:27: warning: no 'async' operations occur within 'await' expression
14108 |                     await completionGate.value
14109 |                     try Task.checkCancellation()
14110 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14111 |                         return
14112 |                     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14117:20: warning: no 'async' operations occur within 'await' expression
14115 |                 if let cursorUTF8Offset,
14116 |                    requestCompletion,
14117 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14118 |                        parse: parse,
14119 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14123:37: warning: no 'async' operations occur within 'await' expression
14121 |                    ) == true
14122 |                 {
14123 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14124 |                         parse: parse,
14125 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[243/249] Compiling BobMacCapture CaptureMoveChoiceView.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:1634:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1632 |         }
1633 | 
1634 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1635 |         return true
1636 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:2461:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2459 |         }
2460 |         if let textView = firstResponder as? NSTextView,
2461 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2462 |            field.accessibilityIdentifier() == identifier
2463 |         {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:10691:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10689 |         newName: String
10690 |     ) {
10691 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10692 |               let rename = current.rename,
10693 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14082:23: warning: no 'async' operations occur within 'await' expression
14080 |                 }
14081 | 
14082 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14083 |                     return
14084 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14095:35: warning: no 'async' operations occur within 'await' expression
14093 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14094 |                         && parse.reportsClipDirective
14095 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14096 |                         draft: draft,
14097 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14110:27: warning: no 'async' operations occur within 'await' expression
14108 |                     await completionGate.value
14109 |                     try Task.checkCancellation()
14110 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14111 |                         return
14112 |                     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14117:20: warning: no 'async' operations occur within 'await' expression
14115 |                 if let cursorUTF8Offset,
14116 |                    requestCompletion,
14117 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14118 |                        parse: parse,
14119 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14123:37: warning: no 'async' operations occur within 'await' expression
14121 |                    ) == true
14122 |                 {
14123 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14124 |                         parse: parse,
14125 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[244/249] Compiling BobMacCapture CapturePanelController.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:1634:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1632 |         }
1633 | 
1634 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1635 |         return true
1636 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:2461:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2459 |         }
2460 |         if let textView = firstResponder as? NSTextView,
2461 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2462 |            field.accessibilityIdentifier() == identifier
2463 |         {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:10691:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10689 |         newName: String
10690 |     ) {
10691 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10692 |               let rename = current.rename,
10693 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14082:23: warning: no 'async' operations occur within 'await' expression
14080 |                 }
14081 | 
14082 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14083 |                     return
14084 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14095:35: warning: no 'async' operations occur within 'await' expression
14093 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14094 |                         && parse.reportsClipDirective
14095 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14096 |                         draft: draft,
14097 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14110:27: warning: no 'async' operations occur within 'await' expression
14108 |                     await completionGate.value
14109 |                     try Task.checkCancellation()
14110 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14111 |                         return
14112 |                     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14117:20: warning: no 'async' operations occur within 'await' expression
14115 |                 if let cursorUTF8Offset,
14116 |                    requestCompletion,
14117 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14118 |                        parse: parse,
14119 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14123:37: warning: no 'async' operations occur within 'await' expression
14121 |                    ) == true
14122 |                 {
14123 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14124 |                         parse: parse,
14125 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[245/249] Compiling BobMacCapture CapturePanelModel.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:1634:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1632 |         }
1633 | 
1634 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1635 |         return true
1636 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:2461:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2459 |         }
2460 |         if let textView = firstResponder as? NSTextView,
2461 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2462 |            field.accessibilityIdentifier() == identifier
2463 |         {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:10691:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10689 |         newName: String
10690 |     ) {
10691 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10692 |               let rename = current.rename,
10693 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14082:23: warning: no 'async' operations occur within 'await' expression
14080 |                 }
14081 | 
14082 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14083 |                     return
14084 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14095:35: warning: no 'async' operations occur within 'await' expression
14093 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14094 |                         && parse.reportsClipDirective
14095 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14096 |                         draft: draft,
14097 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14110:27: warning: no 'async' operations occur within 'await' expression
14108 |                     await completionGate.value
14109 |                     try Task.checkCancellation()
14110 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14111 |                         return
14112 |                     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14117:20: warning: no 'async' operations occur within 'await' expression
14115 |                 if let cursorUTF8Offset,
14116 |                    requestCompletion,
14117 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14118 |                        parse: parse,
14119 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14123:37: warning: no 'async' operations occur within 'await' expression
14121 |                    ) == true
14122 |                 {
14123 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14124 |                         parse: parse,
14125 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[246/249] Compiling BobMacCapture CapturePanelView.swift
/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:373:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
373 |             + Text(String(title[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
374 |     }
375 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CaptureMoveChoiceView.swift:372:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
370 |         else { return Text(title) }
371 |         return Text(String(title[..<range.lowerBound]))
372 |             + Text(String(title[range])).bold().foregroundColor(.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
373 |             + Text(String(title[range.upperBound...]))
374 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:1634:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1632 |         }
1633 | 
1634 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1635 |         return true
1636 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelController.swift:2461:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2459 |         }
2460 |         if let textView = firstResponder as? NSTextView,
2461 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2462 |            field.accessibilityIdentifier() == identifier
2463 |         {

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:2929:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2927 |                         requireInboxRouteChoice: true,
 2928 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2929 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2930 |                     )
 2931 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:10691:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
10689 |         newName: String
10690 |     ) {
10691 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
10692 |               let rename = current.rename,
10693 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14082:23: warning: no 'async' operations occur within 'await' expression
14080 |                 }
14081 | 
14082 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
14083 |                     return
14084 |                 }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14095:35: warning: no 'async' operations occur within 'await' expression
14093 |                         CaptureGrammarGate.isCompatible(parse.grammar)
14094 |                         && parse.reportsClipDirective
14095 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
14096 |                         draft: draft,
14097 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14110:27: warning: no 'async' operations occur within 'await' expression
14108 |                     await completionGate.value
14109 |                     try Task.checkCancellation()
14110 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
14111 |                         return
14112 |                     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14117:20: warning: no 'async' operations occur within 'await' expression
14115 |                 if let cursorUTF8Offset,
14116 |                    requestCompletion,
14117 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
14118 |                        parse: parse,
14119 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelModel.swift:14123:37: warning: no 'async' operations occur within 'await' expression
14121 |                    ) == true
14122 |                 {
14123 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
14124 |                         parse: parse,
14125 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2816:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
2816 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2817 |     }
2818 | 

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:2815:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2813 |         }
2814 |         return Text(String(label[..<range.lowerBound]))
2815 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2816 |             + Text(String(label[range.upperBound...]))
2817 |     }

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3609:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3607 |                     + Text("●").foregroundStyle(
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3610 |                     .font(.caption)
3611 |                     .lineLimit(1)

/private/tmp/bob-cli-h4.4-verify.evdb7uQZ/Sources/BobMacCapture/CapturePanelView.swift:3607:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3605 |             if parts.count == 2 {
3606 |                 (Text(parts[0]).foregroundStyle(.secondary)
3607 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3608 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3609 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[246/249] Write Objects.LinkFileList
[247/249] Linking BobMacCapture
[248/249] Applying BobMacCapture
Build complete! (145.89s)
PASS BobMacCaptureTests
PASS BobMacCaptureInstallHelperTests
PASS CaptureCoreTests
PASS RefsCoreTests
Type-check only: macOS test targets were checked against a stub; CI still runs the tests.
PASS: macOS release bundle and every test target type-check
Remote scratch cleanup verified: /private/tmp/bob-cli-h4.4-verify.evdb7uQZ
succeeded  exit=0  duration=411348ms

