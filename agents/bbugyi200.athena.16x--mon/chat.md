# Chat History - ace-run (16x--mon)

- **TIMESTAMP:** 2026-11-02 07:13:05 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** 16x--mon

## Prompt

sase monitor start --command 'bash -lc \'remote_tmp="$(ssh mac "mktemp -d /tmp/bob-mac-capture-agenda-icon-links.XXXXXX")" || exit $?; trap \'"\'"\'ssh mac "rm -rf -- \\"$remote_tmp\\""\'"\'"\' EXIT; rsync -a --exclude=.git --exclude=.build ./ "mac:${remote_tmp}/" && ssh mac "cd \'"\'"\'$remote_tmp\'"\'"\' && ./Scripts/bundle.sh && just typecheck-tests"\'' --reason 'Type-check the changed Bob Mac Capture targets on macOS'

## Response

sase tool run 7c660db8dc8a3fa2818fa3e98f8083ae
X11 forwarding request failed on channel 0
X11 forwarding request failed on channel 0
Building for production...
[0/6] Write sources
[3/6] Write swift-version--1AB21518FC5DEDBE.txt
[5/7] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8234:13: warning: no calls to throwing functions occur within 'try' expression
8232 |         let container = try decoder.singleValueContainer()
8233 |         // Explicit null has no value; treat it as absent.
8234 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
8235 |             throw DecodingError.valueNotFound(
8236 |                 CaptureThemeSuggestion.self,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[6/8] Compiling RefsCore HighlightsSaveScan.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:1511:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1509 |         }
1510 | 
1511 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1512 |         return true
1513 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:2211:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2209 |         }
2210 |         if let textView = firstResponder as? NSTextView,
2211 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2212 |            field.accessibilityIdentifier() == identifier
2213 |         {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:9161:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 9159 |         newName: String
 9160 |     ) {
 9161 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 9162 |               let rename = current.rename,
 9163 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12322:23: warning: no 'async' operations occur within 'await' expression
12320 |                 }
12321 | 
12322 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
12323 |                     return
12324 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12335:35: warning: no 'async' operations occur within 'await' expression
12333 |                         CaptureGrammarGate.isCompatible(parse.grammar)
12334 |                         && parse.reportsClipDirective
12335 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
12336 |                         draft: draft,
12337 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12350:27: warning: no 'async' operations occur within 'await' expression
12348 |                     await completionGate.value
12349 |                     try Task.checkCancellation()
12350 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
12351 |                         return
12352 |                     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12357:20: warning: no 'async' operations occur within 'await' expression
12355 |                 if let cursorUTF8Offset,
12356 |                    requestCompletion,
12357 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
12358 |                        parse: parse,
12359 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12363:37: warning: no 'async' operations occur within 'await' expression
12361 |                    ) == true
12362 |                 {
12363 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
12364 |                         parse: parse,
12365 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2520:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
2520 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2521 |     }
2522 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2519:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2517 |         }
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2520 |             + Text(String(label[range.upperBound...]))
2521 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3312:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3310 |                     + Text("●").foregroundStyle(
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3313 |                     .font(.caption)
3314 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3310:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3308 |             if parts.count == 2 {
3309 |                 (Text(parts[0]).foregroundStyle(.secondary)
3310 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:372:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 370 | 
 371 |     private var projectedLinksAccessibilityLabel: String {
 372 |         guard let capsule = choice.projectedLinksCapsuleText,
     |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 373 |             let budget = choice.planBudget,
 374 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:805:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 803 |             let chunk = Text("\(separator)\(entry.element.text)")
 804 |                 .foregroundStyle(entry.element.tint ?? .secondary)
 805 |             return result + chunk
     |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 806 |         }
 807 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
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
Build of product 'BobMacCapture' complete! (189.61s)
/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/.build/bundle/Bob Mac Capture.app/Contents/MacOS/BobMacCapture: replacing existing signature
/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/.build/bundle/Bob Mac Capture.app: replacing existing signature
/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/.build/bundle/Bob Mac Capture.app
./Scripts/typecheck-tests.sh
Building for debugging...
[0/18] Write sources
[5/18] Write BobMacCaptureInstallHelper-entitlement.plist
[5/18] Write refs-rank-entitlement.plist
[7/18] Write BobMacCapture-entitlement.plist
[8/18] Write swift-version--1AB21518FC5DEDBE.txt
[10/93] Compiling CaptureCore CaptureTaskCompletePresentation.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[11/93] Compiling CaptureCore CaptureTaskThemePresentation.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[12/93] Compiling CaptureCore CaptureTaskTypeMenuPresentation.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[13/93] Compiling CaptureCore CaptureTextRanges.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[14/93] Compiling CaptureCore CaptureTodayPomodoroGoto.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[15/93] Compiling CaptureCore CaptureTogglePresentation.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[16/93] Compiling CaptureCore CaptureUnconfiguredThemePresentation.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[17/93] Compiling CaptureCore CompletionRowContent.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[18/93] Compiling CaptureCore DependencyPickerPresentation.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[19/93] Compiling CaptureCore FuzzyMatcher.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[20/103] Emitting module CaptureCore
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[21/103] Compiling CaptureCore CaptureAgendaHold.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[22/103] Compiling CaptureCore CaptureAgendaInlineText.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[23/103] Compiling CaptureCore CaptureAgendaLayout.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[24/103] Compiling CaptureCore CaptureAgendaModels.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[25/103] Compiling CaptureCore CaptureAgendaPresentation.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[26/103] Compiling CaptureCore CaptureAgendaRefreshFilter.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[27/103] Compiling CaptureCore CaptureAgendaRefreshState.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[28/103] Compiling CaptureCore CaptureAgendaVisibility.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[29/103] Compiling CaptureCore CaptureBlockDiffRow.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[30/103] Compiling CaptureCore CaptureBlockIDSplice.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[31/103] Compiling CaptureCore CaptureClipPresentation.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[32/103] Compiling CaptureCore ObsidianOpenURL.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[33/103] Compiling CaptureCore ParentTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[34/103] Compiling CaptureCore PomodoroHomes.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[35/103] Compiling CaptureCore SimilarTasksBandEdits.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[36/103] Compiling CaptureCore SimilarTasksBandPolicy.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[37/103] Compiling CaptureCore SimilarTasksBandPresentation.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[38/103] Compiling CaptureCore TaskCompletePickerPresentation.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[39/103] Compiling CaptureCore TaskDisplayText.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[40/103] Compiling CaptureCore TaskLinkPickerPresentation.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[41/103] Compiling CaptureCore WikilinkTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[42/103] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[43/103] Compiling CaptureCore BlockIDPickerIndex.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[44/103] Compiling CaptureCore BlockIDRules.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[45/103] Compiling CaptureCore BobEnvironment.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[46/103] Compiling CaptureCore BobErrors.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[47/103] Compiling CaptureCore BobExecutableResolver.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[48/103] Compiling CaptureCore BobMacCaptureLaunchContext.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[49/103] Compiling CaptureCore BobProcessClient.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[50/103] Compiling CaptureCore CanceledDraftStashStore.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[51/103] Compiling CaptureCore CaptureAgendaBoundaryRefresh.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[52/103] Compiling CaptureCore CaptureAgendaFitPlanner.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8435:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8433 | }
8434 | 
8435 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
8436 |     public let replacement: String
8437 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[53/103] Compiling CaptureCore CaptureOpenHintPresentation.swift
[54/103] Compiling CaptureCore CaptureOpenPlan.swift
[55/103] Compiling CaptureCore CapturePanelPlacement.swift
[56/103] Compiling CaptureCore CapturePickerHelpers.swift
[57/103] Compiling CaptureCore CapturePickerPresentation.swift
[58/103] Compiling CaptureCore CapturePlanBudgetPresentation.swift
[59/103] Compiling CaptureCore CapturePomodoroAdjustPresentation.swift
[60/103] Compiling CaptureCore CapturePomodoroBlockPresentation.swift
[61/103] Compiling CaptureCore CapturePomodoroClosePresentation.swift
[62/103] Compiling CaptureCore CapturePomodoroLineTokens.swift
[63/103] Compiling CaptureCore CapturePomodoroLinkPresentation.swift
[64/103] Compiling CaptureCore CaptureRelationCloseEffect.swift
[65/103] Compiling CaptureCore CaptureRelationCompletePresentation.swift
[66/103] Compiling CaptureCore CaptureRelationshipCopy.swift
[67/103] Compiling CaptureCore CaptureRelationshipPresentation.swift
[68/103] Compiling CaptureCore CaptureSavedTemplates.swift
[69/103] Compiling CaptureCore CaptureSubBulletPresentation.swift
[70/103] Compiling CaptureCore CaptureSuccessorOfferRows.swift
[71/103] Compiling CaptureCore CaptureSuccessorPresentation.swift
[72/103] Compiling CaptureCore CaptureTargetsCache.swift
[73/103] Compiling CaptureCore CaptureTaskBlockPresentation.swift
[74/103] Compiling CaptureCore CaptureCloseTaskCommaAssist.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8234:13: warning: no calls to throwing functions occur within 'try' expression
8232 |         let container = try decoder.singleValueContainer()
8233 |         // Explicit null has no value; treat it as absent.
8234 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
8235 |             throw DecodingError.valueNotFound(
8236 |                 CaptureThemeSuggestion.self,
[75/103] Compiling CaptureCore CaptureCloseTaskCommaProvenance.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8234:13: warning: no calls to throwing functions occur within 'try' expression
8232 |         let container = try decoder.singleValueContainer()
8233 |         // Explicit null has no value; treat it as absent.
8234 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
8235 |             throw DecodingError.valueNotFound(
8236 |                 CaptureThemeSuggestion.self,
[76/103] Compiling CaptureCore CaptureCompletionMenu.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8234:13: warning: no calls to throwing functions occur within 'try' expression
8232 |         let container = try decoder.singleValueContainer()
8233 |         // Explicit null has no value; treat it as absent.
8234 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
8235 |             throw DecodingError.valueNotFound(
8236 |                 CaptureThemeSuggestion.self,
[77/103] Compiling CaptureCore CaptureDrawerMenuPresentation.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8234:13: warning: no calls to throwing functions occur within 'try' expression
8232 |         let container = try decoder.singleValueContainer()
8233 |         // Explicit null has no value; treat it as absent.
8234 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
8235 |             throw DecodingError.valueNotFound(
8236 |                 CaptureThemeSuggestion.self,
[78/103] Compiling CaptureCore CaptureEditWrite.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8234:13: warning: no calls to throwing functions occur within 'try' expression
8232 |         let container = try decoder.singleValueContainer()
8233 |         // Explicit null has no value; treat it as absent.
8234 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
8235 |             throw DecodingError.valueNotFound(
8236 |                 CaptureThemeSuggestion.self,
[79/103] Compiling CaptureCore CaptureGrammarGate.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8234:13: warning: no calls to throwing functions occur within 'try' expression
8232 |         let container = try decoder.singleValueContainer()
8233 |         // Explicit null has no value; treat it as absent.
8234 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
8235 |             throw DecodingError.valueNotFound(
8236 |                 CaptureThemeSuggestion.self,
[80/103] Compiling CaptureCore CaptureInboxRoutePresentation.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8234:13: warning: no calls to throwing functions occur within 'try' expression
8232 |         let container = try decoder.singleValueContainer()
8233 |         // Explicit null has no value; treat it as absent.
8234 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
8235 |             throw DecodingError.valueNotFound(
8236 |                 CaptureThemeSuggestion.self,
[81/103] Compiling CaptureCore CaptureLineCaseToggle.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8234:13: warning: no calls to throwing functions occur within 'try' expression
8232 |         let container = try decoder.singleValueContainer()
8233 |         // Explicit null has no value; treat it as absent.
8234 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
8235 |             throw DecodingError.valueNotFound(
8236 |                 CaptureThemeSuggestion.self,
[82/103] Compiling CaptureCore CaptureLinkGuardPresentation.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8234:13: warning: no calls to throwing functions occur within 'try' expression
8232 |         let container = try decoder.singleValueContainer()
8233 |         // Explicit null has no value; treat it as absent.
8234 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
8235 |             throw DecodingError.valueNotFound(
8236 |                 CaptureThemeSuggestion.self,
[83/103] Compiling CaptureCore CaptureList.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8234:13: warning: no calls to throwing functions occur within 'try' expression
8232 |         let container = try decoder.singleValueContainer()
8233 |         // Explicit null has no value; treat it as absent.
8234 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
8235 |             throw DecodingError.valueNotFound(
8236 |                 CaptureThemeSuggestion.self,
[84/103] Compiling CaptureCore CaptureModels.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/CaptureCore/CaptureModels.swift:8234:13: warning: no calls to throwing functions occur within 'try' expression
8232 |         let container = try decoder.singleValueContainer()
8233 |         // Explicit null has no value; treat it as absent.
8234 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
8235 |             throw DecodingError.valueNotFound(
8236 |                 CaptureThemeSuggestion.self,
[85/103] Compiling CaptureCore CapturePomodoroMergePresentation.swift
[86/103] Compiling CaptureCore CapturePomodoroResetPresentation.swift
[87/103] Compiling CaptureCore CapturePomodoroShiftPresentation.swift
[88/103] Compiling CaptureCore CapturePomodoroSplitPresentation.swift
[89/103] Compiling CaptureCore CapturePomodoroStartPresentation.swift
[90/103] Compiling CaptureCore CaptureProjectNotePresentation.swift
[91/103] Compiling CaptureCore CaptureRefFileUnder.swift
[92/103] Compiling CaptureCore CaptureRefPresentation.swift
[93/103] Compiling CaptureCore CaptureRelatedModels.swift
[94/103] Compiling CaptureCore CaptureRelationCancelPresentation.swift
[95/138] Compiling RefsCore RefsStores.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[96/138] Compiling RefsCore RefsTabClose.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[97/138] Compiling RefsCore RefsTabsRanking.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[98/138] Compiling RefsCore RefsToday.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[99/142] Compiling RefsCore RefsScan.swift
[100/142] Compiling RefsCore RefsScanReceipt.swift
[101/142] Compiling RefsCore RefsSectionedWindow.swift
[102/142] Compiling RefsCore RefsSelection.swift
[103/142] Compiling RefsCore RefsModel.swift
[104/142] Compiling RefsCore RefsNew.swift
[105/142] Compiling RefsCore RefsNewest.swift
[106/142] Compiling RefsCore RefsPDFUpdates.swift
[107/142] Compiling RefsCore RefsDecoding.swift
[108/142] Compiling RefsCore RefsFetching.swift
[109/142] Compiling RefsCore RefsHighlightPicker.swift
[110/142] Compiling RefsCore RefsHighlightsTabs.swift
[111/142] Compiling RefsCore RefsPanelGeometry.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[112/142] Compiling RefsCore RefsQuoteUnderline.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[113/142] Compiling RefsCore RefsRanking.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[114/142] Compiling RefsCore RefsRename.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[115/142] Compiling RefsCore RefsInspector.swift
[116/142] Compiling RefsCore RefsInspectorImages.swift
[117/142] Compiling RefsCore RefsLinks.swift
[118/142] Compiling RefsCore RefsListScroll.swift
[119/142] Compiling RefsCore HighlightsSaveScan.swift
[120/142] Compiling RefsCore RefsArrivals.swift
[121/142] Compiling RefsCore RefsCaption.swift
[122/142] Compiling RefsCore RefsCode.swift
[123/142] Compiling RefsCore RefsCopy.swift
[124/142] Emitting module RefsCore
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[125/142] Compiling RefsCore RefsTodayLinkCard.swift
[126/142] Compiling RefsCore RefsTodayLinkModels.swift
[127/142] Compiling RefsCore RefsTodayLinkPresentation.swift
[128/142] Compiling RefsCore RefsWatcherRelevance.swift
[129/222] Compiling refs_rank main.swift
[130/222] Emitting module refs_rank
[130/222] Write Objects.LinkFileList
[131/222] Linking refs-rank
[132/222] Applying refs-rank
[134/222] Emitting module BobMacCaptureInstallHelper
[135/222] Compiling BobMacCaptureInstallHelper InstallHelperArguments.swift
[136/222] Compiling BobMacCaptureInstallHelper InstallRelauncher.swift
[137/222] Compiling BobMacCaptureInstallHelper InstallHelperError.swift
[138/222] Compiling BobMacCaptureInstallHelper BobMacCaptureInstallHelperMain.swift
[138/222] Write Objects.LinkFileList
[139/222] Linking BobMacCaptureInstallHelper
[140/222] Applying BobMacCaptureInstallHelper
[142/222] Emitting module BobMacCapture
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[143/233] Compiling BobMacCapture AccessibilityTrust.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[144/233] Compiling BobMacCapture AppDelegate.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[145/233] Compiling BobMacCapture AppRelauncher.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[146/233] Compiling BobMacCapture AppSettings.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[147/233] Compiling BobMacCapture BlockDiffCard.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[148/233] Compiling BobMacCapture BlockIDField.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[149/233] Compiling BobMacCapture BobMacCaptureMain.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[150/233] Compiling BobMacCapture BobPanelCoordinator.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[151/233] Compiling BobMacCapture BundleSigningInspector.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[152/233] Compiling BobMacCapture CanceledDraftStash.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[153/233] Compiling BobMacCapture CaptureAgendaRowMeasurer.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[#TrailingClosureMatching]: <https://docs.swift.org/compiler/documentation/diagnostics/trailing-closure-matching>
[154/233] Compiling BobMacCapture RefsScanReceiptObserver.swift
[155/233] Compiling BobMacCapture RefsSearchBar.swift
[156/233] Compiling BobMacCapture RefsTabsViews.swift
[157/233] Compiling BobMacCapture RefsTodayLinkCardView.swift
[158/233] Compiling BobMacCapture RefsUnderlineRenderer.swift
[159/233] Compiling BobMacCapture RefsVisualTokens.swift
[160/233] Compiling BobMacCapture RefsAliasHotkeyRegistration.swift
[161/233] Compiling BobMacCapture RefsHighlightsCodeKey.swift
[162/233] Compiling BobMacCapture RefsHighlightsCopyKey.swift
[163/233] Compiling BobMacCapture RefsHighlightsLinkKey.swift
[164/233] Compiling BobMacCapture RefsHighlightsOpenKey.swift
[165/233] Compiling BobMacCapture CaptureTaskTypeMenuView.swift
[166/233] Compiling BobMacCapture ClipCardView.swift
[167/233] Compiling BobMacCapture HighlightsSaveKeyMonitor.swift
[168/233] Compiling BobMacCapture HighlightsTakeover.swift
[169/233] Compiling BobMacCapture HotKeyRegistry.swift
[170/233] Compiling BobMacCapture NotificationService.swift
[171/233] Compiling BobMacCapture PlainTextPaste.swift
[172/233] Compiling BobMacCapture PomodoroBlockView.swift
[173/233] Compiling BobMacCapture PomodoroHomeColor.swift
[174/233] Compiling BobMacCapture PomodoroNameField.swift
[175/233] Compiling BobMacCapture PomodoroThemeViews.swift
[176/233] Compiling BobMacCapture RefsHighlightsTabsKey.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[177/233] Compiling BobMacCapture RefsHotkeyRegistration.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[178/233] Compiling BobMacCapture RelationLabelField.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[179/233] Compiling BobMacCapture SavedTemplateShelf.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[180/233] Compiling BobMacCapture SettingsView.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[181/233] Compiling BobMacCapture Signposts.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[182/233] Compiling BobMacCapture SimilarTasksBandView.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[183/233] Compiling BobMacCapture StatusItemController.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[184/233] Compiling BobMacCapture StatusItemGlyph.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[185/233] Compiling BobMacCapture TaskBlockView.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[186/233] Compiling BobMacCapture VaultTargetWatcher.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[187/233] Compiling BobMacCapture AXHighlightsTabsReader.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[188/233] Compiling BobMacCapture RefsActionsMenu.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[189/233] Compiling BobMacCapture RefsAnnotationImages.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[190/233] Compiling BobMacCapture RefsCodePreviewWell.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[191/233] Compiling BobMacCapture RefsCopyCardView.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[192/233] Compiling BobMacCapture RefsCopyHUD.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[193/233] Compiling BobMacCapture RefsFooter.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[194/233] Compiling BobMacCapture RefsInspectorImageViews.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[195/233] Compiling BobMacCapture RefsInspectorLoader.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[196/233] Compiling BobMacCapture RefsInspectorScroll.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[197/233] Compiling BobMacCapture RefsInspectorView.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[198/233] Compiling BobMacCapture RefsKeyRouter.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[199/233] Compiling BobMacCapture RefsLibrary.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[200/233] Compiling BobMacCapture RefsLinkPreviewWell.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[201/233] Compiling BobMacCapture RefsListView.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[202/233] Compiling BobMacCapture RefsPanel.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[203/233] Compiling BobMacCapture RefsPanelModel.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[204/233] Compiling BobMacCapture RefsPanelStates.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[205/233] Compiling BobMacCapture RefsPanelView.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[206/233] Compiling BobMacCapture RefsQuoteText.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[207/233] Compiling BobMacCapture RefsRenameCardView.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[208/233] Compiling BobMacCapture RefsRowView.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[209/233] Compiling BobMacCapture CaptureAgendaStore.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:1511:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1509 |         }
1510 | 
1511 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1512 |         return true
1513 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:2211:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2209 |         }
2210 |         if let textView = firstResponder as? NSTextView,
2211 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2212 |            field.accessibilityIdentifier() == identifier
2213 |         {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:9161:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 9159 |         newName: String
 9160 |     ) {
 9161 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 9162 |               let rename = current.rename,
 9163 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12322:23: warning: no 'async' operations occur within 'await' expression
12320 |                 }
12321 | 
12322 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
12323 |                     return
12324 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12335:35: warning: no 'async' operations occur within 'await' expression
12333 |                         CaptureGrammarGate.isCompatible(parse.grammar)
12334 |                         && parse.reportsClipDirective
12335 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
12336 |                         draft: draft,
12337 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12350:27: warning: no 'async' operations occur within 'await' expression
12348 |                     await completionGate.value
12349 |                     try Task.checkCancellation()
12350 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
12351 |                         return
12352 |                     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12357:20: warning: no 'async' operations occur within 'await' expression
12355 |                 if let cursorUTF8Offset,
12356 |                    requestCompletion,
12357 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
12358 |                        parse: parse,
12359 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12363:37: warning: no 'async' operations occur within 'await' expression
12361 |                    ) == true
12362 |                 {
12363 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
12364 |                         parse: parse,
12365 |                         cursor: cursorUTF8Offset,

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[210/233] Compiling BobMacCapture CaptureAgendaView.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:1511:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1509 |         }
1510 | 
1511 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1512 |         return true
1513 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:2211:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2209 |         }
2210 |         if let textView = firstResponder as? NSTextView,
2211 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2212 |            field.accessibilityIdentifier() == identifier
2213 |         {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:9161:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 9159 |         newName: String
 9160 |     ) {
 9161 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 9162 |               let rename = current.rename,
 9163 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12322:23: warning: no 'async' operations occur within 'await' expression
12320 |                 }
12321 | 
12322 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
12323 |                     return
12324 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12335:35: warning: no 'async' operations occur within 'await' expression
12333 |                         CaptureGrammarGate.isCompatible(parse.grammar)
12334 |                         && parse.reportsClipDirective
12335 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
12336 |                         draft: draft,
12337 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12350:27: warning: no 'async' operations occur within 'await' expression
12348 |                     await completionGate.value
12349 |                     try Task.checkCancellation()
12350 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
12351 |                         return
12352 |                     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12357:20: warning: no 'async' operations occur within 'await' expression
12355 |                 if let cursorUTF8Offset,
12356 |                    requestCompletion,
12357 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
12358 |                        parse: parse,
12359 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12363:37: warning: no 'async' operations occur within 'await' expression
12361 |                    ) == true
12362 |                 {
12363 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
12364 |                         parse: parse,
12365 |                         cursor: cursorUTF8Offset,

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[211/233] Compiling BobMacCapture CaptureAliasHotkeyRegistration.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:1511:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1509 |         }
1510 | 
1511 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1512 |         return true
1513 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:2211:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2209 |         }
2210 |         if let textView = firstResponder as? NSTextView,
2211 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2212 |            field.accessibilityIdentifier() == identifier
2213 |         {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:9161:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 9159 |         newName: String
 9160 |     ) {
 9161 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 9162 |               let rename = current.rename,
 9163 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12322:23: warning: no 'async' operations occur within 'await' expression
12320 |                 }
12321 | 
12322 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
12323 |                     return
12324 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12335:35: warning: no 'async' operations occur within 'await' expression
12333 |                         CaptureGrammarGate.isCompatible(parse.grammar)
12334 |                         && parse.reportsClipDirective
12335 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
12336 |                         draft: draft,
12337 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12350:27: warning: no 'async' operations occur within 'await' expression
12348 |                     await completionGate.value
12349 |                     try Task.checkCancellation()
12350 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
12351 |                         return
12352 |                     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12357:20: warning: no 'async' operations occur within 'await' expression
12355 |                 if let cursorUTF8Offset,
12356 |                    requestCompletion,
12357 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
12358 |                        parse: parse,
12359 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12363:37: warning: no 'async' operations occur within 'await' expression
12361 |                    ) == true
12362 |                 {
12363 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
12364 |                         parse: parse,
12365 |                         cursor: cursorUTF8Offset,

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[212/233] Compiling BobMacCapture CaptureDrawerMenuView.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:1511:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1509 |         }
1510 | 
1511 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1512 |         return true
1513 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:2211:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2209 |         }
2210 |         if let textView = firstResponder as? NSTextView,
2211 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2212 |            field.accessibilityIdentifier() == identifier
2213 |         {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:9161:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 9159 |         newName: String
 9160 |     ) {
 9161 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 9162 |               let rename = current.rename,
 9163 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12322:23: warning: no 'async' operations occur within 'await' expression
12320 |                 }
12321 | 
12322 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
12323 |                     return
12324 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12335:35: warning: no 'async' operations occur within 'await' expression
12333 |                         CaptureGrammarGate.isCompatible(parse.grammar)
12334 |                         && parse.reportsClipDirective
12335 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
12336 |                         draft: draft,
12337 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12350:27: warning: no 'async' operations occur within 'await' expression
12348 |                     await completionGate.value
12349 |                     try Task.checkCancellation()
12350 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
12351 |                         return
12352 |                     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12357:20: warning: no 'async' operations occur within 'await' expression
12355 |                 if let cursorUTF8Offset,
12356 |                    requestCompletion,
12357 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
12358 |                        parse: parse,
12359 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12363:37: warning: no 'async' operations occur within 'await' expression
12361 |                    ) == true
12362 |                 {
12363 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
12364 |                         parse: parse,
12365 |                         cursor: cursorUTF8Offset,

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[213/233] Compiling BobMacCapture CaptureEditorPalette.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:1511:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1509 |         }
1510 | 
1511 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1512 |         return true
1513 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:2211:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2209 |         }
2210 |         if let textView = firstResponder as? NSTextView,
2211 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2212 |            field.accessibilityIdentifier() == identifier
2213 |         {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:9161:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 9159 |         newName: String
 9160 |     ) {
 9161 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 9162 |               let rename = current.rename,
 9163 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12322:23: warning: no 'async' operations occur within 'await' expression
12320 |                 }
12321 | 
12322 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
12323 |                     return
12324 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12335:35: warning: no 'async' operations occur within 'await' expression
12333 |                         CaptureGrammarGate.isCompatible(parse.grammar)
12334 |                         && parse.reportsClipDirective
12335 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
12336 |                         draft: draft,
12337 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12350:27: warning: no 'async' operations occur within 'await' expression
12348 |                     await completionGate.value
12349 |                     try Task.checkCancellation()
12350 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
12351 |                         return
12352 |                     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12357:20: warning: no 'async' operations occur within 'await' expression
12355 |                 if let cursorUTF8Offset,
12356 |                    requestCompletion,
12357 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
12358 |                        parse: parse,
12359 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12363:37: warning: no 'async' operations occur within 'await' expression
12361 |                    ) == true
12362 |                 {
12363 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
12364 |                         parse: parse,
12365 |                         cursor: cursorUTF8Offset,

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[214/233] Compiling BobMacCapture CaptureEditorTextConfiguration.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:1511:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1509 |         }
1510 | 
1511 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1512 |         return true
1513 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:2211:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2209 |         }
2210 |         if let textView = firstResponder as? NSTextView,
2211 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2212 |            field.accessibilityIdentifier() == identifier
2213 |         {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:9161:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 9159 |         newName: String
 9160 |     ) {
 9161 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 9162 |               let rename = current.rename,
 9163 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12322:23: warning: no 'async' operations occur within 'await' expression
12320 |                 }
12321 | 
12322 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
12323 |                     return
12324 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12335:35: warning: no 'async' operations occur within 'await' expression
12333 |                         CaptureGrammarGate.isCompatible(parse.grammar)
12334 |                         && parse.reportsClipDirective
12335 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
12336 |                         draft: draft,
12337 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12350:27: warning: no 'async' operations occur within 'await' expression
12348 |                     await completionGate.value
12349 |                     try Task.checkCancellation()
12350 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
12351 |                         return
12352 |                     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12357:20: warning: no 'async' operations occur within 'await' expression
12355 |                 if let cursorUTF8Offset,
12356 |                    requestCompletion,
12357 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
12358 |                        parse: parse,
12359 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12363:37: warning: no 'async' operations occur within 'await' expression
12361 |                    ) == true
12362 |                 {
12363 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
12364 |                         parse: parse,
12365 |                         cursor: cursorUTF8Offset,

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[215/233] Compiling BobMacCapture CaptureInboxRouteChoiceView.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:1511:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1509 |         }
1510 | 
1511 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1512 |         return true
1513 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:2211:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2209 |         }
2210 |         if let textView = firstResponder as? NSTextView,
2211 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2212 |            field.accessibilityIdentifier() == identifier
2213 |         {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:9161:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 9159 |         newName: String
 9160 |     ) {
 9161 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 9162 |               let rename = current.rename,
 9163 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12322:23: warning: no 'async' operations occur within 'await' expression
12320 |                 }
12321 | 
12322 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
12323 |                     return
12324 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12335:35: warning: no 'async' operations occur within 'await' expression
12333 |                         CaptureGrammarGate.isCompatible(parse.grammar)
12334 |                         && parse.reportsClipDirective
12335 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
12336 |                         draft: draft,
12337 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12350:27: warning: no 'async' operations occur within 'await' expression
12348 |                     await completionGate.value
12349 |                     try Task.checkCancellation()
12350 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
12351 |                         return
12352 |                     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12357:20: warning: no 'async' operations occur within 'await' expression
12355 |                 if let cursorUTF8Offset,
12356 |                    requestCompletion,
12357 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
12358 |                        parse: parse,
12359 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12363:37: warning: no 'async' operations occur within 'await' expression
12361 |                    ) == true
12362 |                 {
12363 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
12364 |                         parse: parse,
12365 |                         cursor: cursorUTF8Offset,

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[216/233] Compiling BobMacCapture CaptureKeyCommandRouter.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:1511:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1509 |         }
1510 | 
1511 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1512 |         return true
1513 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:2211:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2209 |         }
2210 |         if let textView = firstResponder as? NSTextView,
2211 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2212 |            field.accessibilityIdentifier() == identifier
2213 |         {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:9161:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 9159 |         newName: String
 9160 |     ) {
 9161 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 9162 |               let rename = current.rename,
 9163 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12322:23: warning: no 'async' operations occur within 'await' expression
12320 |                 }
12321 | 
12322 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
12323 |                     return
12324 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12335:35: warning: no 'async' operations occur within 'await' expression
12333 |                         CaptureGrammarGate.isCompatible(parse.grammar)
12334 |                         && parse.reportsClipDirective
12335 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
12336 |                         draft: draft,
12337 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12350:27: warning: no 'async' operations occur within 'await' expression
12348 |                     await completionGate.value
12349 |                     try Task.checkCancellation()
12350 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
12351 |                         return
12352 |                     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12357:20: warning: no 'async' operations occur within 'await' expression
12355 |                 if let cursorUTF8Offset,
12356 |                    requestCompletion,
12357 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
12358 |                        parse: parse,
12359 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12363:37: warning: no 'async' operations occur within 'await' expression
12361 |                    ) == true
12362 |                 {
12363 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
12364 |                         parse: parse,
12365 |                         cursor: cursorUTF8Offset,

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[217/233] Compiling BobMacCapture CaptureListGroupCapsule.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:1511:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1509 |         }
1510 | 
1511 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1512 |         return true
1513 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:2211:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2209 |         }
2210 |         if let textView = firstResponder as? NSTextView,
2211 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2212 |            field.accessibilityIdentifier() == identifier
2213 |         {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:9161:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 9159 |         newName: String
 9160 |     ) {
 9161 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 9162 |               let rename = current.rename,
 9163 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12322:23: warning: no 'async' operations occur within 'await' expression
12320 |                 }
12321 | 
12322 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
12323 |                     return
12324 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12335:35: warning: no 'async' operations occur within 'await' expression
12333 |                         CaptureGrammarGate.isCompatible(parse.grammar)
12334 |                         && parse.reportsClipDirective
12335 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
12336 |                         draft: draft,
12337 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12350:27: warning: no 'async' operations occur within 'await' expression
12348 |                     await completionGate.value
12349 |                     try Task.checkCancellation()
12350 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
12351 |                         return
12352 |                     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12357:20: warning: no 'async' operations occur within 'await' expression
12355 |                 if let cursorUTF8Offset,
12356 |                    requestCompletion,
12357 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
12358 |                        parse: parse,
12359 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12363:37: warning: no 'async' operations occur within 'await' expression
12361 |                    ) == true
12362 |                 {
12363 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
12364 |                         parse: parse,
12365 |                         cursor: cursorUTF8Offset,

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[218/233] Compiling BobMacCapture CapturePanelController.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:1511:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1509 |         }
1510 | 
1511 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1512 |         return true
1513 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:2211:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2209 |         }
2210 |         if let textView = firstResponder as? NSTextView,
2211 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2212 |            field.accessibilityIdentifier() == identifier
2213 |         {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:9161:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 9159 |         newName: String
 9160 |     ) {
 9161 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 9162 |               let rename = current.rename,
 9163 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12322:23: warning: no 'async' operations occur within 'await' expression
12320 |                 }
12321 | 
12322 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
12323 |                     return
12324 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12335:35: warning: no 'async' operations occur within 'await' expression
12333 |                         CaptureGrammarGate.isCompatible(parse.grammar)
12334 |                         && parse.reportsClipDirective
12335 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
12336 |                         draft: draft,
12337 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12350:27: warning: no 'async' operations occur within 'await' expression
12348 |                     await completionGate.value
12349 |                     try Task.checkCancellation()
12350 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
12351 |                         return
12352 |                     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12357:20: warning: no 'async' operations occur within 'await' expression
12355 |                 if let cursorUTF8Offset,
12356 |                    requestCompletion,
12357 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
12358 |                        parse: parse,
12359 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12363:37: warning: no 'async' operations occur within 'await' expression
12361 |                    ) == true
12362 |                 {
12363 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
12364 |                         parse: parse,
12365 |                         cursor: cursorUTF8Offset,

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[219/233] Compiling BobMacCapture CapturePanelModel.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:81:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 79 |         processClient: BobProcessClient? = nil,
 80 |         vaultRootPath: String = "",
 81 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 82 |         now: @Sendable @escaping () -> Date = { Date() },
 83 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:371:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
369 |                 Task { [weak self] in
370 |                     await MainActor.run {
371 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
372 |                     }
373 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:384:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
382 |                 Task { [weak self] in
383 |                     await MainActor.run {
384 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
385 |                     }
386 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:397:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
395 |                 Task { [weak self] in
396 |                     await MainActor.run {
397 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
398 |                     }
399 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaStore.swift:410:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
408 |                 Task { [weak self] in
409 |                     await MainActor.run {
410 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
411 |                     }
412 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureAgendaView.swift:1529:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1527 |         for segment in parsed.segments {
1528 |             let slice = String(chars[segment.range])
1529 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1530 |         }
1531 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:1511:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1509 |         }
1510 | 
1511 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1512 |         return true
1513 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelController.swift:2211:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2209 |         }
2210 |         if let textView = firstResponder as? NSTextView,
2211 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2212 |            field.accessibilityIdentifier() == identifier
2213 |         {

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:2669:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2667 |                         requireInboxRouteChoice: true,
 2668 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2669 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2670 |                     )
 2671 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:9161:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 9159 |         newName: String
 9160 |     ) {
 9161 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 9162 |               let rename = current.rename,
 9163 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12322:23: warning: no 'async' operations occur within 'await' expression
12320 |                 }
12321 | 
12322 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
12323 |                     return
12324 |                 }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12335:35: warning: no 'async' operations occur within 'await' expression
12333 |                         CaptureGrammarGate.isCompatible(parse.grammar)
12334 |                         && parse.reportsClipDirective
12335 |                     previewTask = await self?.startLivePreview(
      |                                   `- warning: no 'async' operations occur within 'await' expression
12336 |                         draft: draft,
12337 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12350:27: warning: no 'async' operations occur within 'await' expression
12348 |                     await completionGate.value
12349 |                     try Task.checkCancellation()
12350 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
12351 |                         return
12352 |                     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12357:20: warning: no 'async' operations occur within 'await' expression
12355 |                 if let cursorUTF8Offset,
12356 |                    requestCompletion,
12357 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
12358 |                        parse: parse,
12359 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelModel.swift:12363:37: warning: no 'async' operations occur within 'await' expression
12361 |                    ) == true
12362 |                 {
12363 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
12364 |                         parse: parse,
12365 |                         cursor: cursorUTF8Offset,

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[220/233] Compiling BobMacCapture CapturePanelView.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2520:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
2520 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2521 |     }
2522 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2519:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2517 |         }
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2520 |             + Text(String(label[range.upperBound...]))
2521 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3312:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3310 |                     + Text("●").foregroundStyle(
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3313 |                     .font(.caption)
3314 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3310:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3308 |             if parts.count == 2 {
3309 |                 (Text(parts[0]).foregroundStyle(.secondary)
3310 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:372:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 370 | 
 371 |     private var projectedLinksAccessibilityLabel: String {
 372 |         guard let capsule = choice.projectedLinksCapsuleText,
     |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 373 |             let budget = choice.planBudget,
 374 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:805:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 803 |             let chunk = Text("\(separator)\(entry.element.text)")
 804 |                 .foregroundStyle(entry.element.tint ?? .secondary)
 805 |             return result + chunk
     |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 806 |         }
 807 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[221/233] Compiling BobMacCapture CapturePanelWindowSizer.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2520:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
2520 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2521 |     }
2522 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2519:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2517 |         }
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2520 |             + Text(String(label[range.upperBound...]))
2521 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3312:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3310 |                     + Text("●").foregroundStyle(
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3313 |                     .font(.caption)
3314 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3310:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3308 |             if parts.count == 2 {
3309 |                 (Text(parts[0]).foregroundStyle(.secondary)
3310 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:372:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 370 | 
 371 |     private var projectedLinksAccessibilityLabel: String {
 372 |         guard let capsule = choice.projectedLinksCapsuleText,
     |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 373 |             let budget = choice.planBudget,
 374 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:805:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 803 |             let chunk = Text("\(separator)\(entry.element.text)")
 804 |                 .foregroundStyle(entry.element.tint ?? .secondary)
 805 |             return result + chunk
     |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 806 |         }
 807 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[222/233] Compiling BobMacCapture CapturePickerFilterField.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2520:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
2520 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2521 |     }
2522 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2519:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2517 |         }
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2520 |             + Text(String(label[range.upperBound...]))
2521 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3312:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3310 |                     + Text("●").foregroundStyle(
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3313 |                     .font(.caption)
3314 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3310:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3308 |             if parts.count == 2 {
3309 |                 (Text(parts[0]).foregroundStyle(.secondary)
3310 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:372:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 370 | 
 371 |     private var projectedLinksAccessibilityLabel: String {
 372 |         guard let capsule = choice.projectedLinksCapsuleText,
     |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 373 |             let budget = choice.planBudget,
 374 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:805:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 803 |             let chunk = Text("\(separator)\(entry.element.text)")
 804 |                 .foregroundStyle(entry.element.tint ?? .secondary)
 805 |             return result + chunk
     |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 806 |         }
 807 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[223/233] Compiling BobMacCapture CapturePickerState.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2520:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
2520 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2521 |     }
2522 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2519:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2517 |         }
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2520 |             + Text(String(label[range.upperBound...]))
2521 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3312:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3310 |                     + Text("●").foregroundStyle(
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3313 |                     .font(.caption)
3314 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3310:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3308 |             if parts.count == 2 {
3309 |                 (Text(parts[0]).foregroundStyle(.secondary)
3310 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:372:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 370 | 
 371 |     private var projectedLinksAccessibilityLabel: String {
 372 |         guard let capsule = choice.projectedLinksCapsuleText,
     |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 373 |             let budget = choice.planBudget,
 374 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:805:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 803 |             let chunk = Text("\(separator)\(entry.element.text)")
 804 |                 .foregroundStyle(entry.element.tint ?? .secondary)
 805 |             return result + chunk
     |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 806 |         }
 807 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[224/233] Compiling BobMacCapture CapturePickerView.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2520:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
2520 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2521 |     }
2522 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2519:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2517 |         }
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2520 |             + Text(String(label[range.upperBound...]))
2521 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3312:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3310 |                     + Text("●").foregroundStyle(
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3313 |                     .font(.caption)
3314 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3310:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3308 |             if parts.count == 2 {
3309 |                 (Text(parts[0]).foregroundStyle(.secondary)
3310 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:372:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 370 | 
 371 |     private var projectedLinksAccessibilityLabel: String {
 372 |         guard let capsule = choice.projectedLinksCapsuleText,
     |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 373 |             let budget = choice.planBudget,
 374 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:805:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 803 |             let chunk = Text("\(separator)\(entry.element.text)")
 804 |                 .foregroundStyle(entry.element.tint ?? .secondary)
 805 |             return result + chunk
     |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 806 |         }
 807 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[225/233] Compiling BobMacCapture CapturePlanBudgetMeterRow.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2520:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
2520 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2521 |     }
2522 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2519:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2517 |         }
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2520 |             + Text(String(label[range.upperBound...]))
2521 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3312:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3310 |                     + Text("●").foregroundStyle(
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3313 |                     .font(.caption)
3314 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3310:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3308 |             if parts.count == 2 {
3309 |                 (Text(parts[0]).foregroundStyle(.secondary)
3310 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:372:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 370 | 
 371 |     private var projectedLinksAccessibilityLabel: String {
 372 |         guard let capsule = choice.projectedLinksCapsuleText,
     |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 373 |             let budget = choice.planBudget,
 374 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:805:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 803 |             let chunk = Text("\(separator)\(entry.element.text)")
 804 |                 .foregroundStyle(entry.element.tint ?? .secondary)
 805 |             return result + chunk
     |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 806 |         }
 807 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[226/233] Compiling BobMacCapture CapturePullInChoice.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2520:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
2520 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2521 |     }
2522 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2519:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2517 |         }
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2520 |             + Text(String(label[range.upperBound...]))
2521 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3312:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3310 |                     + Text("●").foregroundStyle(
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3313 |                     .font(.caption)
3314 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3310:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3308 |             if parts.count == 2 {
3309 |                 (Text(parts[0]).foregroundStyle(.secondary)
3310 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:372:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 370 | 
 371 |     private var projectedLinksAccessibilityLabel: String {
 372 |         guard let capsule = choice.projectedLinksCapsuleText,
     |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 373 |             let budget = choice.planBudget,
 374 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:805:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 803 |             let chunk = Text("\(separator)\(entry.element.text)")
 804 |                 .foregroundStyle(entry.element.tint ?? .secondary)
 805 |             return result + chunk
     |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 806 |         }
 807 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[227/233] Compiling BobMacCapture CapturePullInChoiceView.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2520:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
2520 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2521 |     }
2522 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2519:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2517 |         }
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2520 |             + Text(String(label[range.upperBound...]))
2521 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3312:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3310 |                     + Text("●").foregroundStyle(
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3313 |                     .font(.caption)
3314 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3310:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3308 |             if parts.count == 2 {
3309 |                 (Text(parts[0]).foregroundStyle(.secondary)
3310 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:372:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 370 | 
 371 |     private var projectedLinksAccessibilityLabel: String {
 372 |         guard let capsule = choice.projectedLinksCapsuleText,
     |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 373 |             let budget = choice.planBudget,
 374 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:805:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 803 |             let chunk = Text("\(separator)\(entry.element.text)")
 804 |                 .foregroundStyle(entry.element.tint ?? .secondary)
 805 |             return result + chunk
     |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 806 |         }
 807 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[228/233] Compiling BobMacCapture CaptureShowRefreshWindow.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2520:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
2520 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2521 |     }
2522 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2519:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2517 |         }
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2520 |             + Text(String(label[range.upperBound...]))
2521 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3312:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3310 |                     + Text("●").foregroundStyle(
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3313 |                     .font(.caption)
3314 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3310:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3308 |             if parts.count == 2 {
3309 |                 (Text(parts[0]).foregroundStyle(.secondary)
3310 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:372:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 370 | 
 371 |     private var projectedLinksAccessibilityLabel: String {
 372 |         guard let capsule = choice.projectedLinksCapsuleText,
     |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 373 |             let budget = choice.planBudget,
 374 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:805:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 803 |             let chunk = Text("\(separator)\(entry.element.text)")
 804 |                 .foregroundStyle(entry.element.tint ?? .secondary)
 805 |             return result + chunk
     |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 806 |         }
 807 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[229/233] Compiling BobMacCapture CaptureSnippetResolver.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2520:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
2520 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2521 |     }
2522 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2519:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2517 |         }
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2520 |             + Text(String(label[range.upperBound...]))
2521 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3312:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3310 |                     + Text("●").foregroundStyle(
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3313 |                     .font(.caption)
3314 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3310:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3308 |             if parts.count == 2 {
3309 |                 (Text(parts[0]).foregroundStyle(.secondary)
3310 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:372:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 370 | 
 371 |     private var projectedLinksAccessibilityLabel: String {
 372 |         guard let capsule = choice.projectedLinksCapsuleText,
     |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 373 |             let budget = choice.planBudget,
 374 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:805:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 803 |             let chunk = Text("\(separator)\(entry.element.text)")
 804 |                 .foregroundStyle(entry.element.tint ?? .secondary)
 805 |             return result + chunk
     |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 806 |         }
 807 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[230/233] Compiling BobMacCapture CaptureTargetsRefreshGate.swift
/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2520:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
2520 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2521 |     }
2522 | 

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:2519:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2517 |         }
2518 |         return Text(String(label[..<range.lowerBound]))
2519 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2520 |             + Text(String(label[range.upperBound...]))
2521 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3312:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3310 |                     + Text("●").foregroundStyle(
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3313 |                     .font(.caption)
3314 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePanelView.swift:3310:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3308 |             if parts.count == 2 {
3309 |                 (Text(parts[0]).foregroundStyle(.secondary)
3310 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3311 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3312 |                     + Text(parts[1]).foregroundStyle(.secondary))

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:372:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 370 | 
 371 |     private var projectedLinksAccessibilityLabel: String {
 372 |         guard let capsule = choice.projectedLinksCapsuleText,
     |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
 373 |             let budget = choice.planBudget,
 374 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CapturePullInChoiceView.swift:805:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 803 |             let chunk = Text("\(separator)\(entry.element.text)")
 804 |                 .foregroundStyle(entry.element.tint ?? .secondary)
 805 |             return result + chunk
     |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
 806 |         }
 807 |     }

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-agenda-icon-links.2TXGJW/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[230/233] Write Objects.LinkFileList
[231/233] Linking BobMacCapture
[232/233] Applying BobMacCapture
Build complete! (81.68s)
PASS BobMacCaptureTests
PASS BobMacCaptureInstallHelperTests
PASS CaptureCoreTests
PASS RefsCoreTests
Type-check only: macOS test targets were checked against a stub; CI still runs the tests.
X11 forwarding request failed on channel 0
succeeded  exit=0  duration=292075ms

