# Chat History - ace-run (163--mon)

- **TIMESTAMP:** 2026-10-30 09:57:49 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** 163--mon

## Prompt

sase monitor start --command '/tmp/run-wikilink-task-mac-verification.sh' --reason 'Run the approved Mac Capture scratch bundle and test typecheck, then verify the current working tree in hosted macOS CI'

## Response

sase tool run c894b1ea042ce25d9ce914f91a88862b
X11 forwarding request failed on channel 0
Building for debugging...
[0/8] Write sources
[3/8] Write BobMacCapture-entitlement.plist
[4/8] Write swift-version--1AB21518FC5DEDBE.txt
[6/73] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[7/73] Compiling CaptureCore BlockIDPickerIndex.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[8/73] Compiling CaptureCore BlockIDRules.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[9/73] Compiling CaptureCore BobEnvironment.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[10/73] Compiling CaptureCore BobErrors.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[11/73] Compiling CaptureCore BobExecutableResolver.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[12/73] Compiling CaptureCore BobMacCaptureLaunchContext.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[13/73] Compiling CaptureCore BobProcessClient.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[14/73] Compiling CaptureCore CanceledDraftStashStore.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[15/73] Compiling CaptureCore CaptureAgendaFitPlanner.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[16/73] Emitting module CaptureCore
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BlockIDPickerIndex.swift:916:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 914 | /// section 40%, status name 30%.
 915 | private struct BlockIDLinkEntry: Sendable {
 916 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 917 |     let bobIndex: Int
 918 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:450:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
448 | /// locator stays searchable.
449 | struct WikilinkTaskPickerIndexEntry: Sendable {
450 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
451 |     let bobIndex: Int
452 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[17/73] Compiling CaptureCore CaptureRelationshipCopy.swift
[18/73] Compiling CaptureCore CaptureRelationshipPresentation.swift
[19/73] Compiling CaptureCore CaptureSavedTemplates.swift
[20/73] Compiling CaptureCore CaptureSubBulletPresentation.swift
[21/73] Compiling CaptureCore CaptureSuccessorPresentation.swift
[22/73] Compiling CaptureCore CaptureTargetsCache.swift
[23/73] Compiling CaptureCore CaptureTaskBlockPresentation.swift
[24/73] Compiling CaptureCore CaptureTaskCompletePresentation.swift
[25/73] Compiling CaptureCore CaptureTaskThemePresentation.swift
[26/73] Compiling CaptureCore CapturePickerHelpers.swift
[27/73] Compiling CaptureCore CapturePickerPresentation.swift
[28/73] Compiling CaptureCore CapturePlanBudgetPresentation.swift
[29/73] Compiling CaptureCore CapturePomodoroAdjustPresentation.swift
[30/73] Compiling CaptureCore CapturePomodoroBlockPresentation.swift
[31/73] Compiling CaptureCore CapturePomodoroClosePresentation.swift
[32/73] Compiling CaptureCore CapturePomodoroLineTokens.swift
[33/73] Compiling CaptureCore CapturePomodoroLinkPresentation.swift
[34/73] Compiling CaptureCore CapturePomodoroResetPresentation.swift
[35/73] Compiling CaptureCore CapturePomodoroShiftPresentation.swift
[36/73] Compiling CaptureCore CapturePomodoroStartPresentation.swift
[37/73] Compiling CaptureCore CaptureProjectNotePresentation.swift
[38/73] Compiling CaptureCore CaptureRefFileUnder.swift
[39/73] Compiling CaptureCore CaptureRefPresentation.swift
[40/73] Compiling CaptureCore CaptureRelatedModels.swift
[41/73] Compiling CaptureCore CaptureRelationCancelPresentation.swift
[42/73] Compiling CaptureCore CaptureRelationCloseEffect.swift
[43/73] Compiling CaptureCore CaptureRelationCompletePresentation.swift
[44/82] Compiling CaptureCore ParentTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:450:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
448 | /// locator stays searchable.
449 | struct WikilinkTaskPickerIndexEntry: Sendable {
450 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
451 |     let bobIndex: Int
452 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[45/82] Compiling CaptureCore PomodoroHomes.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:450:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
448 | /// locator stays searchable.
449 | struct WikilinkTaskPickerIndexEntry: Sendable {
450 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
451 |     let bobIndex: Int
452 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[46/82] Compiling CaptureCore SimilarTasksBandEdits.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:450:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
448 | /// locator stays searchable.
449 | struct WikilinkTaskPickerIndexEntry: Sendable {
450 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
451 |     let bobIndex: Int
452 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[47/82] Compiling CaptureCore SimilarTasksBandPolicy.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:450:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
448 | /// locator stays searchable.
449 | struct WikilinkTaskPickerIndexEntry: Sendable {
450 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
451 |     let bobIndex: Int
452 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[48/82] Compiling CaptureCore SimilarTasksBandPresentation.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:450:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
448 | /// locator stays searchable.
449 | struct WikilinkTaskPickerIndexEntry: Sendable {
450 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
451 |     let bobIndex: Int
452 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[49/82] Compiling CaptureCore TaskCompletePickerPresentation.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:450:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
448 | /// locator stays searchable.
449 | struct WikilinkTaskPickerIndexEntry: Sendable {
450 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
451 |     let bobIndex: Int
452 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[50/82] Compiling CaptureCore TaskDisplayText.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:450:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
448 | /// locator stays searchable.
449 | struct WikilinkTaskPickerIndexEntry: Sendable {
450 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
451 |     let bobIndex: Int
452 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[51/82] Compiling CaptureCore TaskLinkPickerPresentation.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:450:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
448 | /// locator stays searchable.
449 | struct WikilinkTaskPickerIndexEntry: Sendable {
450 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
451 |     let bobIndex: Int
452 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[52/82] Compiling CaptureCore WikilinkTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/ParentTaskPickerPresentation.swift:514:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
512 | 
513 | private struct ParentTaskPickerIndexEntry: Sendable {
514 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
515 |     let bobIndex: Int
516 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:450:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
448 | /// locator stays searchable.
449 | struct WikilinkTaskPickerIndexEntry: Sendable {
450 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
451 |     let bobIndex: Int
452 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[53/82] Compiling CaptureCore CaptureTemplateStart.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[54/82] Compiling CaptureCore CaptureTextRanges.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[55/82] Compiling CaptureCore CaptureTodayPomodoroGoto.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[56/82] Compiling CaptureCore CaptureTogglePresentation.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[57/82] Compiling CaptureCore CaptureUnconfiguredThemePresentation.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[58/82] Compiling CaptureCore CompletionRowContent.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[59/82] Compiling CaptureCore DependencyPickerPresentation.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[60/82] Compiling CaptureCore FuzzyMatcher.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[61/82] Compiling CaptureCore ObsidianOpenURL.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7665:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7663 | }
7664 | 
7665 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
     |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
7666 |     public let replacement: String
7667 |     public let route: String?
[62/82] Compiling CaptureCore CaptureCloseTaskCommaAssist.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7495:13: warning: no calls to throwing functions occur within 'try' expression
7493 |         let container = try decoder.singleValueContainer()
7494 |         // Explicit null has no value; treat it as absent.
7495 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
7496 |             throw DecodingError.valueNotFound(
7497 |                 CaptureThemeSuggestion.self,
[63/82] Compiling CaptureCore CaptureCloseTaskCommaProvenance.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7495:13: warning: no calls to throwing functions occur within 'try' expression
7493 |         let container = try decoder.singleValueContainer()
7494 |         // Explicit null has no value; treat it as absent.
7495 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
7496 |             throw DecodingError.valueNotFound(
7497 |                 CaptureThemeSuggestion.self,
[64/82] Compiling CaptureCore CaptureEditWrite.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7495:13: warning: no calls to throwing functions occur within 'try' expression
7493 |         let container = try decoder.singleValueContainer()
7494 |         // Explicit null has no value; treat it as absent.
7495 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
7496 |             throw DecodingError.valueNotFound(
7497 |                 CaptureThemeSuggestion.self,
[65/82] Compiling CaptureCore CaptureInboxRoutePresentation.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7495:13: warning: no calls to throwing functions occur within 'try' expression
7493 |         let container = try decoder.singleValueContainer()
7494 |         // Explicit null has no value; treat it as absent.
7495 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
7496 |             throw DecodingError.valueNotFound(
7497 |                 CaptureThemeSuggestion.self,
[66/82] Compiling CaptureCore CaptureLinkGuardPresentation.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7495:13: warning: no calls to throwing functions occur within 'try' expression
7493 |         let container = try decoder.singleValueContainer()
7494 |         // Explicit null has no value; treat it as absent.
7495 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
7496 |             throw DecodingError.valueNotFound(
7497 |                 CaptureThemeSuggestion.self,
[67/82] Compiling CaptureCore CaptureModels.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7495:13: warning: no calls to throwing functions occur within 'try' expression
7493 |         let container = try decoder.singleValueContainer()
7494 |         // Explicit null has no value; treat it as absent.
7495 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
7496 |             throw DecodingError.valueNotFound(
7497 |                 CaptureThemeSuggestion.self,
[68/82] Compiling CaptureCore CaptureOpenHintPresentation.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7495:13: warning: no calls to throwing functions occur within 'try' expression
7493 |         let container = try decoder.singleValueContainer()
7494 |         // Explicit null has no value; treat it as absent.
7495 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
7496 |             throw DecodingError.valueNotFound(
7497 |                 CaptureThemeSuggestion.self,
[69/82] Compiling CaptureCore CaptureOpenPlan.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7495:13: warning: no calls to throwing functions occur within 'try' expression
7493 |         let container = try decoder.singleValueContainer()
7494 |         // Explicit null has no value; treat it as absent.
7495 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
7496 |             throw DecodingError.valueNotFound(
7497 |                 CaptureThemeSuggestion.self,
[70/82] Compiling CaptureCore CapturePanelPlacement.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureModels.swift:7495:13: warning: no calls to throwing functions occur within 'try' expression
7493 |         let container = try decoder.singleValueContainer()
7494 |         // Explicit null has no value; treat it as absent.
7495 |         if (try? container.decodeNil()) == true {
     |             `- warning: no calls to throwing functions occur within 'try' expression
7496 |             throw DecodingError.valueNotFound(
7497 |                 CaptureThemeSuggestion.self,
[71/82] Compiling CaptureCore CaptureAgendaHold.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[72/82] Compiling CaptureCore CaptureAgendaInlineText.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[73/82] Compiling CaptureCore CaptureAgendaLayout.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[74/82] Compiling CaptureCore CaptureAgendaModels.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[75/82] Compiling CaptureCore CaptureAgendaPresentation.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[76/82] Compiling CaptureCore CaptureAgendaRefreshFilter.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[77/82] Compiling CaptureCore CaptureAgendaRefreshState.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[78/82] Compiling CaptureCore CaptureAgendaVisibility.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[79/82] Compiling CaptureCore CaptureBlockDiffRow.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/CaptureCore/CaptureAgendaLayout.swift:258:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
256 |             return nil
257 |         }
258 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
259 |         let components = DateComponents(
260 |             year: year,
[80/112] Compiling RefsCore RefsStores.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[81/112] Compiling RefsCore RefsTabClose.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[82/112] Compiling RefsCore RefsTabsRanking.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[83/112] Compiling RefsCore RefsToday.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[84/112] Compiling RefsCore RefsScan.swift
[85/112] Compiling RefsCore RefsScanReceipt.swift
[86/112] Compiling RefsCore RefsSectionedWindow.swift
[87/112] Compiling RefsCore RefsSelection.swift
[88/116] Compiling RefsCore RefsModel.swift
[89/116] Compiling RefsCore RefsNew.swift
[90/116] Compiling RefsCore RefsNewest.swift
[91/116] Compiling RefsCore RefsPDFUpdates.swift
[92/116] Compiling RefsCore RefsInspector.swift
[93/116] Compiling RefsCore RefsInspectorImages.swift
[94/116] Compiling RefsCore RefsLinks.swift
[95/116] Compiling RefsCore RefsListScroll.swift
[96/116] Compiling RefsCore RefsPanelGeometry.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[97/116] Compiling RefsCore RefsQuoteUnderline.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[98/116] Compiling RefsCore RefsRanking.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[99/116] Compiling RefsCore RefsRename.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsRename.swift:17:12: warning: no calls to throwing functions occur within 'try' expression
 15 |     public init(from decoder: Decoder) throws {
 16 |         let container = try decoder.singleValueContainer()
 17 |         if try container.decodeNil() {
    |            `- warning: no calls to throwing functions occur within 'try' expression
 18 |             self = .null
 19 |         } else if let value = try? container.decode(Bool.self) {
[100/116] Compiling RefsCore RefsDecoding.swift
[101/116] Compiling RefsCore RefsFetching.swift
[102/116] Compiling RefsCore RefsHighlightPicker.swift
[103/116] Compiling RefsCore RefsHighlightsTabs.swift
[104/116] Compiling RefsCore HighlightsSaveScan.swift
[105/116] Compiling RefsCore RefsArrivals.swift
[106/116] Compiling RefsCore RefsCaption.swift
[107/116] Compiling RefsCore RefsCode.swift
[108/116] Compiling RefsCore RefsCopy.swift
[109/116] Emitting module RefsCore
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsStores.swift:43:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsSnapshotStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsStores.swift:184:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsOpenLogStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/RefsCore/RefsStores.swift:378:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'RefsNewMarkStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[110/116] Compiling RefsCore RefsTodayLinkCard.swift
[111/116] Compiling RefsCore RefsTodayLinkModels.swift
[112/116] Compiling RefsCore RefsTodayLinkPresentation.swift
[113/116] Compiling RefsCore RefsWatcherRelevance.swift
[114/191] Compiling BobMacCapture RefsTabsViews.swift
[115/191] Compiling BobMacCapture RefsTodayLinkCardView.swift
[116/191] Compiling BobMacCapture RefsUnderlineRenderer.swift
[117/191] Compiling BobMacCapture RefsVisualTokens.swift
[118/191] Compiling BobMacCapture RefsAliasHotkeyRegistration.swift
[119/191] Compiling BobMacCapture RefsHighlightsCodeKey.swift
[120/191] Compiling BobMacCapture RefsHighlightsCopyKey.swift
[121/191] Compiling BobMacCapture RefsHighlightsLinkKey.swift
[122/191] Compiling BobMacCapture RefsHighlightsOpenKey.swift
[123/191] Compiling BobMacCapture RefsHighlightsTabsKey.swift
[124/201] Compiling BobMacCapture RefsHotkeyRegistration.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[125/201] Compiling BobMacCapture RelationLabelField.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[126/201] Compiling BobMacCapture SavedTemplateShelf.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[127/201] Compiling BobMacCapture SettingsView.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[128/201] Compiling BobMacCapture Signposts.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[129/201] Compiling BobMacCapture SimilarTasksBandView.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[130/201] Compiling BobMacCapture StatusItemController.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[131/201] Compiling BobMacCapture StatusItemGlyph.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[132/201] Compiling BobMacCapture TaskBlockView.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[133/201] Compiling BobMacCapture VaultTargetWatcher.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/SimilarTasksBandView.swift:330:26: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
328 |                 part = part.fontWeight(.semibold)
329 |             }
330 |             return soFar + part
    |                          `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
331 |         }
332 |     }

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[134/201] Compiling BobMacCapture RefsCopyCardView.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[135/201] Compiling BobMacCapture RefsCopyHUD.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[136/201] Compiling BobMacCapture RefsFooter.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[137/201] Compiling BobMacCapture RefsInspectorImageViews.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[138/201] Compiling BobMacCapture RefsInspectorLoader.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[139/201] Compiling BobMacCapture RefsInspectorScroll.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[140/201] Compiling BobMacCapture RefsInspectorView.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[141/201] Compiling BobMacCapture RefsKeyRouter.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[142/201] Compiling BobMacCapture RefsLibrary.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[143/201] Compiling BobMacCapture RefsLinkPreviewWell.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:683:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
683 |             + Text(String(row.preview[range.upperBound...]))
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
684 |                 .foregroundStyle(.secondary)
685 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsCopyCardView.swift:682:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
680 |         return Text(String(row.preview[..<range.lowerBound]))
681 |             .foregroundStyle(.secondary)
682 |             + Text("●").foregroundStyle(Color.accentColor)
    |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
683 |             + Text(String(row.preview[range.upperBound...]))
684 |                 .foregroundStyle(.secondary)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:682:27: warning: expression of type 'Bool' is unused [#no-usage]
 680 |     private func refreshSnapshotAfterRename() async {
 681 |         while let current = snapshotTask {
 682 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 683 |         }
 684 |         refreshSnapshot(reason: .manual)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:686:27: warning: expression of type 'Bool' is unused [#no-usage]
 684 |         refreshSnapshot(reason: .manual)
 685 |         while let current = snapshotTask {
 686 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 687 |         }
 688 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:954:27: warning: expression of type 'Bool' is unused [#no-usage]
 952 |     private func runPostScanRefresh() async {
 953 |         while let current = snapshotTask {
 954 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 955 |             if snapshotTask == nil {
 956 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:961:27: warning: expression of type 'Bool' is unused [#no-usage]
 959 |         refresh(reason: .scan)
 960 |         while let current = snapshotTask {
 961 |             await current.value
     |                           `- warning: expression of type 'Bool' is unused [#no-usage]
 962 |             if snapshotTask == nil {
 963 |                 break

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:1027:24: warning: no 'async' operations occur within 'await' expression
1025 |             },
1026 |             onFailure: { [weak self] message in
1027 |                 Task { await self?.watcherFailed(message) }
     |                        `- warning: no 'async' operations occur within 'await' expression
1028 |             }
1029 |         )

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[144/201] Compiling BobMacCapture CapturePickerFilterField.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[145/201] Compiling BobMacCapture CapturePickerState.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[146/201] Compiling BobMacCapture CapturePickerView.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[147/201] Compiling BobMacCapture CapturePlanBudgetMeterRow.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[148/201] Compiling BobMacCapture CapturePullInChoice.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[149/201] Compiling BobMacCapture CapturePullInChoiceView.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[150/201] Compiling BobMacCapture CaptureShowRefreshWindow.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[151/201] Compiling BobMacCapture CaptureSnippetResolver.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[152/201] Compiling BobMacCapture CaptureTargetsRefreshGate.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[153/201] Compiling BobMacCapture HighlightsSaveKeyMonitor.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[154/201] Compiling BobMacCapture HighlightsTakeover.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:322:19: warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
320 | 
321 |     private var projectedLinksAccessibilityLabel: String {
322 |         guard let capsule = choice.projectedLinksCapsuleText,
    |                   `- warning: immutable value 'capsule' was never used; consider replacing with '_' or removing it [#no-usage]
323 |             let budget = choice.planBudget,
324 |             let projected = choice.projectedLinkCount

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePullInChoiceView.swift:697:27: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
695 |             let chunk = Text("\(separator)\(entry.element.text)")
696 |                 .foregroundStyle(entry.element.tint ?? .secondary)
697 |             return result + chunk
    |                           `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
698 |         }
699 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[155/201] Compiling BobMacCapture AccessibilityTrust.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[156/201] Compiling BobMacCapture AppDelegate.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[157/201] Compiling BobMacCapture AppRelauncher.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[158/201] Compiling BobMacCapture AppSettings.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[159/201] Compiling BobMacCapture BlockDiffCard.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[160/201] Compiling BobMacCapture BlockIDField.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[161/201] Compiling BobMacCapture BobMacCaptureMain.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[162/201] Compiling BobMacCapture BobPanelCoordinator.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[163/201] Compiling BobMacCapture BundleSigningInspector.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[164/201] Compiling BobMacCapture CanceledDraftStash.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[165/201] Compiling BobMacCapture CaptureAgendaRowMeasurer.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:83:53: warning: backward matching of the unlabeled trailing closure is deprecated; label the argument with 'activateApplication' to suppress this warning [#TrailingClosureMatching]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:316:55: warning: use '#selector' instead of explicitly constructing a 'Selector'
 314 |         menu.addItem(redo)
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
     |                                                       `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
 318 |         menu.addItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:317:56: warning: use '#selector' instead of explicitly constructing a 'Selector'
 315 |         menu.addItem(.separator())
 316 |         menu.addItem(NSMenuItem(title: "Cut", action: Selector(("cut:")), keyEquivalent: "x"))
 317 |         menu.addItem(NSMenuItem(title: "Copy", action: Selector(("copy:")), keyEquivalent: "c"))
     |                                                        `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 318 |         menu.addItem(
 319 |             NSMenuItem(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:326:53: warning: use '#selector' instead of explicitly constructing a 'Selector'
 324 |         )
 325 |         menu.addItem(
 326 |             NSMenuItem(title: "Select All", action: Selector(("selectAll:")), keyEquivalent: "a"))
     |                                                     `- warning: use '#selector' instead of explicitly constructing a 'Selector'
 327 |         return menu
 328 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:625:58: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 623 |     /// off MainActor state.
 624 |     nonisolated static func storedHighlightsAppPath() -> String {
 625 |         UserDefaults.standard.string(forKey: AppSettings.refsHighlightsAppPathKey) ?? ""
     |                                                          `- warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
 626 |     }
 627 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:9:16: note: static property declared here
  7 |     /// Defaults key for the Highlights override path, shared with the
  8 |     /// Sendable locator read in AppDelegate.
  9 |     static let refsHighlightsAppPathKey = "refsHighlightsAppPath"
    |                `- note: static property declared here
 10 | 
 11 |     @Published var bobExecutableOverride: String {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:705:62: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 703 |             library: library,
 704 |             opener: WorkspaceRefsOpener(),
 705 |             highlights: HighlightsLocator(overridePath: Self.storedHighlightsAppPath),
     |                                                              `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 706 |             tabs: tabsSession,
 707 |             isAdHocSigned: { signingState == .adHoc }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:999:26: warning: use '#selector' instead of explicitly constructing a 'Selector'
 997 |             return
 998 |         }
 999 |         NSApp.sendAction(Selector(("paste:")), to: nil, from: sender)
     |                          `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1000 |     }
1001 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[166/201] Compiling BobMacCapture RefsListView.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[167/201] Compiling BobMacCapture RefsPanel.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[168/201] Compiling BobMacCapture RefsPanelModel.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[169/201] Compiling BobMacCapture RefsPanelStates.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[170/201] Compiling BobMacCapture RefsPanelView.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[171/201] Compiling BobMacCapture RefsQuoteText.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[172/201] Compiling BobMacCapture RefsRenameCardView.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[173/201] Compiling BobMacCapture RefsRowView.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[174/201] Compiling BobMacCapture RefsScanReceiptObserver.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[175/201] Compiling BobMacCapture RefsSearchBar.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:310:27: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
308 |                 // rows report nil, which never clears the current rect.
309 |                 .onGeometryChange(for: CGRect?.self) { proxy in
310 |                     model.selectedID == id
    |                           `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
311 |                         ? proxy.frame(in: .named("refsPanel")) : nil
312 |                 } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsListView.swift:358:23: warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
356 |             .transition(removalTransition)
357 |             .onGeometryChange(for: CGRect?.self) { proxy in
358 |                 model.selectedID == id
    |                       `- warning: main actor-isolated property 'selectedID' can not be referenced from a Sendable closure
359 |                     ? proxy.frame(in: .named("refsPanel")) : nil
360 |             } action: { rect in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:413:40: note: property declared here
 411 |         return tabsFilter && tabsListing?.tabs[id] != nil
 412 |     }
 413 |     @Published public private(set) var selectedID: String? {
     |                                        `- note: property declared here
 414 |         didSet {
 415 |             if panelIsVisible(), let selectedID {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:249:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 247 |         completion: @escaping (Error?) -> Void
 248 |     ) {
 249 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 250 |         configuration.activates = true
 251 |         NSWorkspace.shared.open(

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:298:13: warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 296 | 
 297 |     public func openWithDefaultApp(_ url: URL, completion: @escaping (Error?) -> Void) {
 298 |         var configuration = NSWorkspace.OpenConfiguration()
     |             `- warning: variable 'configuration' was never mutated; consider changing to 'let' constant
 299 |         configuration.activates = true
 300 |         NSWorkspace.shared.open(url, configuration: configuration) { _, error in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:804:20: warning: no 'async' operations occur within 'await' expression
 802 |         }.store(in: &subscriptions)
 803 |         library.$refreshState.sink { [weak self] _ in
 804 |             Task { await self?.refreshStateDidChange() }
     |                    `- warning: no 'async' operations occur within 'await' expression
 805 |         }.store(in: &subscriptions)
 806 |         library.onScanStarted = { [weak self] origin, isFollowUp in

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3274:21: warning: no 'async' operations occur within 'await' expression
3272 |             opener.openWithDefaultApp(request.url) { [weak self] error in
3273 |                 Task {
3274 |                     await self?.finishLinkOpen(request, error: error)
     |                     `- warning: no 'async' operations occur within 'await' expression
3275 |                 }
3276 |             }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3703:13: warning: result of call to 'openSelected' is unused [#no-usage]
3701 |             openWithDefaultApp(item)
3702 |         case .note, .reveal, .task:
3703 |             openSelected(pending.target)
     |             `- warning: result of call to 'openSelected' is unused [#no-usage]
3704 |         }
3705 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3740:17: warning: no 'async' operations occur within 'await' expression
3738 |         opener.openInHighlights(closed.url, app: app) { [weak self] error in
3739 |             Task {
3740 |                 await self?.finishClosedTabOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3741 |             }
3742 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3767:17: warning: no 'async' operations occur within 'await' expression
3765 |         opener.openWithDefaultApp(closed.url) { [weak self] error in
3766 |             Task {
3767 |                 await self?.finishClosedTabDefaultAppOpen(closed, error: error)
     |                 `- warning: no 'async' operations occur within 'await' expression
3768 |             }
3769 |         }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3836:17: warning: no 'async' operations occur within 'await' expression
3834 |         opener.openInHighlights(pdf, app: app) { [weak self] error in
3835 |             Task {
3836 |                 await self?.finishHighlightsOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3837 |                     itemID: item.id,
3838 |                     title: item.title.text,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsPanelModel.swift:3867:17: warning: no 'async' operations occur within 'await' expression
3865 |         opener.openWithDefaultApp(pdf) { [weak self] error in
3866 |             Task {
3867 |                 await self?.finishDefaultAppOpen(
     |                 `- warning: no 'async' operations occur within 'await' expression
3868 |                     itemID: item.id,
3869 |                     title: item.title.text,
[176/201] Compiling BobMacCapture CaptureAgendaStore.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:1460:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1458 |         }
1459 | 
1460 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1461 |         return true
1462 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:2108:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2106 |         }
2107 |         if let textView = firstResponder as? NSTextView,
2108 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2109 |            field.accessibilityIdentifier() == identifier
2110 |         {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:8777:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8775 |         newName: String
 8776 |     ) {
 8777 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8778 |               let rename = current.rename,
 8779 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11839:23: warning: no 'async' operations occur within 'await' expression
11837 |                 }
11838 | 
11839 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11840 |                     return
11841 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11844:21: warning: no 'async' operations occur within 'await' expression
11842 | 
11843 |                 if pickerNeeded == nil {
11844 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11845 |                         draft: draft,
11846 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11858:27: warning: no 'async' operations occur within 'await' expression
11856 |                     await completionGate.value
11857 |                     try Task.checkCancellation()
11858 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11859 |                         return
11860 |                     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11865:20: warning: no 'async' operations occur within 'await' expression
11863 |                 if let cursorUTF8Offset,
11864 |                    requestCompletion,
11865 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11866 |                        parse: parse,
11867 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11871:37: warning: no 'async' operations occur within 'await' expression
11869 |                    ) == true
11870 |                 {
11871 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11872 |                         parse: parse,
11873 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:12183:28: warning: no 'async' operations occur within 'await' expression
12181 |         Task { [weak self, processClient] in
12182 |             do {
12183 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
12184 |                 let processClientIdentity = processClient.identityToken
12185 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2477:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
2477 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2478 |     }
2479 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2476:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2474 |         }
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2477 |             + Text(String(label[range.upperBound...]))
2478 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3234:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3232 |                     + Text("●").foregroundStyle(
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3235 |                     .font(.caption)
3236 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3232:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3230 |             if parts.count == 2 {
3231 |                 (Text(parts[0]).foregroundStyle(.secondary)
3232 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[177/201] Compiling BobMacCapture CaptureAgendaView.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:1460:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1458 |         }
1459 | 
1460 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1461 |         return true
1462 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:2108:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2106 |         }
2107 |         if let textView = firstResponder as? NSTextView,
2108 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2109 |            field.accessibilityIdentifier() == identifier
2110 |         {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:8777:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8775 |         newName: String
 8776 |     ) {
 8777 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8778 |               let rename = current.rename,
 8779 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11839:23: warning: no 'async' operations occur within 'await' expression
11837 |                 }
11838 | 
11839 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11840 |                     return
11841 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11844:21: warning: no 'async' operations occur within 'await' expression
11842 | 
11843 |                 if pickerNeeded == nil {
11844 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11845 |                         draft: draft,
11846 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11858:27: warning: no 'async' operations occur within 'await' expression
11856 |                     await completionGate.value
11857 |                     try Task.checkCancellation()
11858 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11859 |                         return
11860 |                     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11865:20: warning: no 'async' operations occur within 'await' expression
11863 |                 if let cursorUTF8Offset,
11864 |                    requestCompletion,
11865 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11866 |                        parse: parse,
11867 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11871:37: warning: no 'async' operations occur within 'await' expression
11869 |                    ) == true
11870 |                 {
11871 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11872 |                         parse: parse,
11873 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:12183:28: warning: no 'async' operations occur within 'await' expression
12181 |         Task { [weak self, processClient] in
12182 |             do {
12183 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
12184 |                 let processClientIdentity = processClient.identityToken
12185 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2477:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
2477 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2478 |     }
2479 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2476:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2474 |         }
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2477 |             + Text(String(label[range.upperBound...]))
2478 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3234:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3232 |                     + Text("●").foregroundStyle(
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3235 |                     .font(.caption)
3236 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3232:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3230 |             if parts.count == 2 {
3231 |                 (Text(parts[0]).foregroundStyle(.secondary)
3232 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[178/201] Compiling BobMacCapture CaptureAliasHotkeyRegistration.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:1460:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1458 |         }
1459 | 
1460 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1461 |         return true
1462 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:2108:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2106 |         }
2107 |         if let textView = firstResponder as? NSTextView,
2108 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2109 |            field.accessibilityIdentifier() == identifier
2110 |         {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:8777:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8775 |         newName: String
 8776 |     ) {
 8777 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8778 |               let rename = current.rename,
 8779 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11839:23: warning: no 'async' operations occur within 'await' expression
11837 |                 }
11838 | 
11839 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11840 |                     return
11841 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11844:21: warning: no 'async' operations occur within 'await' expression
11842 | 
11843 |                 if pickerNeeded == nil {
11844 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11845 |                         draft: draft,
11846 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11858:27: warning: no 'async' operations occur within 'await' expression
11856 |                     await completionGate.value
11857 |                     try Task.checkCancellation()
11858 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11859 |                         return
11860 |                     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11865:20: warning: no 'async' operations occur within 'await' expression
11863 |                 if let cursorUTF8Offset,
11864 |                    requestCompletion,
11865 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11866 |                        parse: parse,
11867 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11871:37: warning: no 'async' operations occur within 'await' expression
11869 |                    ) == true
11870 |                 {
11871 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11872 |                         parse: parse,
11873 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:12183:28: warning: no 'async' operations occur within 'await' expression
12181 |         Task { [weak self, processClient] in
12182 |             do {
12183 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
12184 |                 let processClientIdentity = processClient.identityToken
12185 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2477:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
2477 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2478 |     }
2479 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2476:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2474 |         }
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2477 |             + Text(String(label[range.upperBound...]))
2478 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3234:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3232 |                     + Text("●").foregroundStyle(
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3235 |                     .font(.caption)
3236 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3232:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3230 |             if parts.count == 2 {
3231 |                 (Text(parts[0]).foregroundStyle(.secondary)
3232 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[179/201] Compiling BobMacCapture CaptureEditorPalette.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:1460:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1458 |         }
1459 | 
1460 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1461 |         return true
1462 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:2108:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2106 |         }
2107 |         if let textView = firstResponder as? NSTextView,
2108 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2109 |            field.accessibilityIdentifier() == identifier
2110 |         {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:8777:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8775 |         newName: String
 8776 |     ) {
 8777 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8778 |               let rename = current.rename,
 8779 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11839:23: warning: no 'async' operations occur within 'await' expression
11837 |                 }
11838 | 
11839 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11840 |                     return
11841 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11844:21: warning: no 'async' operations occur within 'await' expression
11842 | 
11843 |                 if pickerNeeded == nil {
11844 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11845 |                         draft: draft,
11846 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11858:27: warning: no 'async' operations occur within 'await' expression
11856 |                     await completionGate.value
11857 |                     try Task.checkCancellation()
11858 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11859 |                         return
11860 |                     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11865:20: warning: no 'async' operations occur within 'await' expression
11863 |                 if let cursorUTF8Offset,
11864 |                    requestCompletion,
11865 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11866 |                        parse: parse,
11867 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11871:37: warning: no 'async' operations occur within 'await' expression
11869 |                    ) == true
11870 |                 {
11871 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11872 |                         parse: parse,
11873 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:12183:28: warning: no 'async' operations occur within 'await' expression
12181 |         Task { [weak self, processClient] in
12182 |             do {
12183 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
12184 |                 let processClientIdentity = processClient.identityToken
12185 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2477:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
2477 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2478 |     }
2479 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2476:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2474 |         }
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2477 |             + Text(String(label[range.upperBound...]))
2478 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3234:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3232 |                     + Text("●").foregroundStyle(
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3235 |                     .font(.caption)
3236 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3232:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3230 |             if parts.count == 2 {
3231 |                 (Text(parts[0]).foregroundStyle(.secondary)
3232 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[180/201] Compiling BobMacCapture CaptureEditorTextConfiguration.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:1460:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1458 |         }
1459 | 
1460 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1461 |         return true
1462 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:2108:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2106 |         }
2107 |         if let textView = firstResponder as? NSTextView,
2108 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2109 |            field.accessibilityIdentifier() == identifier
2110 |         {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:8777:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8775 |         newName: String
 8776 |     ) {
 8777 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8778 |               let rename = current.rename,
 8779 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11839:23: warning: no 'async' operations occur within 'await' expression
11837 |                 }
11838 | 
11839 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11840 |                     return
11841 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11844:21: warning: no 'async' operations occur within 'await' expression
11842 | 
11843 |                 if pickerNeeded == nil {
11844 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11845 |                         draft: draft,
11846 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11858:27: warning: no 'async' operations occur within 'await' expression
11856 |                     await completionGate.value
11857 |                     try Task.checkCancellation()
11858 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11859 |                         return
11860 |                     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11865:20: warning: no 'async' operations occur within 'await' expression
11863 |                 if let cursorUTF8Offset,
11864 |                    requestCompletion,
11865 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11866 |                        parse: parse,
11867 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11871:37: warning: no 'async' operations occur within 'await' expression
11869 |                    ) == true
11870 |                 {
11871 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11872 |                         parse: parse,
11873 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:12183:28: warning: no 'async' operations occur within 'await' expression
12181 |         Task { [weak self, processClient] in
12182 |             do {
12183 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
12184 |                 let processClientIdentity = processClient.identityToken
12185 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2477:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
2477 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2478 |     }
2479 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2476:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2474 |         }
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2477 |             + Text(String(label[range.upperBound...]))
2478 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3234:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3232 |                     + Text("●").foregroundStyle(
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3235 |                     .font(.caption)
3236 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3232:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3230 |             if parts.count == 2 {
3231 |                 (Text(parts[0]).foregroundStyle(.secondary)
3232 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[181/201] Compiling BobMacCapture CaptureInboxRouteChoiceView.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:1460:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1458 |         }
1459 | 
1460 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1461 |         return true
1462 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:2108:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2106 |         }
2107 |         if let textView = firstResponder as? NSTextView,
2108 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2109 |            field.accessibilityIdentifier() == identifier
2110 |         {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:8777:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8775 |         newName: String
 8776 |     ) {
 8777 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8778 |               let rename = current.rename,
 8779 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11839:23: warning: no 'async' operations occur within 'await' expression
11837 |                 }
11838 | 
11839 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11840 |                     return
11841 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11844:21: warning: no 'async' operations occur within 'await' expression
11842 | 
11843 |                 if pickerNeeded == nil {
11844 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11845 |                         draft: draft,
11846 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11858:27: warning: no 'async' operations occur within 'await' expression
11856 |                     await completionGate.value
11857 |                     try Task.checkCancellation()
11858 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11859 |                         return
11860 |                     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11865:20: warning: no 'async' operations occur within 'await' expression
11863 |                 if let cursorUTF8Offset,
11864 |                    requestCompletion,
11865 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11866 |                        parse: parse,
11867 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11871:37: warning: no 'async' operations occur within 'await' expression
11869 |                    ) == true
11870 |                 {
11871 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11872 |                         parse: parse,
11873 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:12183:28: warning: no 'async' operations occur within 'await' expression
12181 |         Task { [weak self, processClient] in
12182 |             do {
12183 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
12184 |                 let processClientIdentity = processClient.identityToken
12185 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2477:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
2477 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2478 |     }
2479 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2476:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2474 |         }
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2477 |             + Text(String(label[range.upperBound...]))
2478 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3234:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3232 |                     + Text("●").foregroundStyle(
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3235 |                     .font(.caption)
3236 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3232:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3230 |             if parts.count == 2 {
3231 |                 (Text(parts[0]).foregroundStyle(.secondary)
3232 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[182/201] Compiling BobMacCapture CaptureKeyCommandRouter.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:1460:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1458 |         }
1459 | 
1460 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1461 |         return true
1462 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:2108:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2106 |         }
2107 |         if let textView = firstResponder as? NSTextView,
2108 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2109 |            field.accessibilityIdentifier() == identifier
2110 |         {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:8777:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8775 |         newName: String
 8776 |     ) {
 8777 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8778 |               let rename = current.rename,
 8779 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11839:23: warning: no 'async' operations occur within 'await' expression
11837 |                 }
11838 | 
11839 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11840 |                     return
11841 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11844:21: warning: no 'async' operations occur within 'await' expression
11842 | 
11843 |                 if pickerNeeded == nil {
11844 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11845 |                         draft: draft,
11846 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11858:27: warning: no 'async' operations occur within 'await' expression
11856 |                     await completionGate.value
11857 |                     try Task.checkCancellation()
11858 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11859 |                         return
11860 |                     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11865:20: warning: no 'async' operations occur within 'await' expression
11863 |                 if let cursorUTF8Offset,
11864 |                    requestCompletion,
11865 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11866 |                        parse: parse,
11867 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11871:37: warning: no 'async' operations occur within 'await' expression
11869 |                    ) == true
11870 |                 {
11871 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11872 |                         parse: parse,
11873 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:12183:28: warning: no 'async' operations occur within 'await' expression
12181 |         Task { [weak self, processClient] in
12182 |             do {
12183 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
12184 |                 let processClientIdentity = processClient.identityToken
12185 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2477:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
2477 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2478 |     }
2479 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2476:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2474 |         }
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2477 |             + Text(String(label[range.upperBound...]))
2478 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3234:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3232 |                     + Text("●").foregroundStyle(
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3235 |                     .font(.caption)
3236 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3232:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3230 |             if parts.count == 2 {
3231 |                 (Text(parts[0]).foregroundStyle(.secondary)
3232 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[183/201] Compiling BobMacCapture CapturePanelController.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:1460:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1458 |         }
1459 | 
1460 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1461 |         return true
1462 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:2108:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2106 |         }
2107 |         if let textView = firstResponder as? NSTextView,
2108 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2109 |            field.accessibilityIdentifier() == identifier
2110 |         {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:8777:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8775 |         newName: String
 8776 |     ) {
 8777 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8778 |               let rename = current.rename,
 8779 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11839:23: warning: no 'async' operations occur within 'await' expression
11837 |                 }
11838 | 
11839 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11840 |                     return
11841 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11844:21: warning: no 'async' operations occur within 'await' expression
11842 | 
11843 |                 if pickerNeeded == nil {
11844 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11845 |                         draft: draft,
11846 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11858:27: warning: no 'async' operations occur within 'await' expression
11856 |                     await completionGate.value
11857 |                     try Task.checkCancellation()
11858 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11859 |                         return
11860 |                     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11865:20: warning: no 'async' operations occur within 'await' expression
11863 |                 if let cursorUTF8Offset,
11864 |                    requestCompletion,
11865 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11866 |                        parse: parse,
11867 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11871:37: warning: no 'async' operations occur within 'await' expression
11869 |                    ) == true
11870 |                 {
11871 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11872 |                         parse: parse,
11873 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:12183:28: warning: no 'async' operations occur within 'await' expression
12181 |         Task { [weak self, processClient] in
12182 |             do {
12183 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
12184 |                 let processClientIdentity = processClient.identityToken
12185 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2477:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
2477 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2478 |     }
2479 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2476:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2474 |         }
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2477 |             + Text(String(label[range.upperBound...]))
2478 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3234:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3232 |                     + Text("●").foregroundStyle(
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3235 |                     .font(.caption)
3236 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3232:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3230 |             if parts.count == 2 {
3231 |                 (Text(parts[0]).foregroundStyle(.secondary)
3232 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[184/201] Compiling BobMacCapture CapturePanelModel.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:1460:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1458 |         }
1459 | 
1460 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1461 |         return true
1462 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:2108:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2106 |         }
2107 |         if let textView = firstResponder as? NSTextView,
2108 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2109 |            field.accessibilityIdentifier() == identifier
2110 |         {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:8777:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8775 |         newName: String
 8776 |     ) {
 8777 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8778 |               let rename = current.rename,
 8779 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11839:23: warning: no 'async' operations occur within 'await' expression
11837 |                 }
11838 | 
11839 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11840 |                     return
11841 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11844:21: warning: no 'async' operations occur within 'await' expression
11842 | 
11843 |                 if pickerNeeded == nil {
11844 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11845 |                         draft: draft,
11846 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11858:27: warning: no 'async' operations occur within 'await' expression
11856 |                     await completionGate.value
11857 |                     try Task.checkCancellation()
11858 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11859 |                         return
11860 |                     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11865:20: warning: no 'async' operations occur within 'await' expression
11863 |                 if let cursorUTF8Offset,
11864 |                    requestCompletion,
11865 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11866 |                        parse: parse,
11867 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11871:37: warning: no 'async' operations occur within 'await' expression
11869 |                    ) == true
11870 |                 {
11871 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11872 |                         parse: parse,
11873 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:12183:28: warning: no 'async' operations occur within 'await' expression
12181 |         Task { [weak self, processClient] in
12182 |             do {
12183 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
12184 |                 let processClientIdentity = processClient.identityToken
12185 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2477:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
2477 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2478 |     }
2479 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2476:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2474 |         }
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2477 |             + Text(String(label[range.upperBound...]))
2478 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3234:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3232 |                     + Text("●").foregroundStyle(
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3235 |                     .font(.caption)
3236 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3232:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3230 |             if parts.count == 2 {
3231 |                 (Text(parts[0]).foregroundStyle(.secondary)
3232 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[185/201] Compiling BobMacCapture CapturePanelView.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:1460:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1458 |         }
1459 | 
1460 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1461 |         return true
1462 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:2108:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2106 |         }
2107 |         if let textView = firstResponder as? NSTextView,
2108 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2109 |            field.accessibilityIdentifier() == identifier
2110 |         {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:8777:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8775 |         newName: String
 8776 |     ) {
 8777 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8778 |               let rename = current.rename,
 8779 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11839:23: warning: no 'async' operations occur within 'await' expression
11837 |                 }
11838 | 
11839 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11840 |                     return
11841 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11844:21: warning: no 'async' operations occur within 'await' expression
11842 | 
11843 |                 if pickerNeeded == nil {
11844 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11845 |                         draft: draft,
11846 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11858:27: warning: no 'async' operations occur within 'await' expression
11856 |                     await completionGate.value
11857 |                     try Task.checkCancellation()
11858 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11859 |                         return
11860 |                     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11865:20: warning: no 'async' operations occur within 'await' expression
11863 |                 if let cursorUTF8Offset,
11864 |                    requestCompletion,
11865 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11866 |                        parse: parse,
11867 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11871:37: warning: no 'async' operations occur within 'await' expression
11869 |                    ) == true
11870 |                 {
11871 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11872 |                         parse: parse,
11873 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:12183:28: warning: no 'async' operations occur within 'await' expression
12181 |         Task { [weak self, processClient] in
12182 |             do {
12183 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
12184 |                 let processClientIdentity = processClient.identityToken
12185 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2477:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
2477 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2478 |     }
2479 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2476:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2474 |         }
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2477 |             + Text(String(label[range.upperBound...]))
2478 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3234:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3232 |                     + Text("●").foregroundStyle(
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3235 |                     .font(.caption)
3236 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3232:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3230 |             if parts.count == 2 {
3231 |                 (Text(parts[0]).foregroundStyle(.secondary)
3232 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[186/201] Compiling BobMacCapture CapturePanelWindowSizer.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:370:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
368 |                 Task { [weak self] in
369 |                     await MainActor.run {
370 |                         self?.refresh(reason: .wake)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
371 |                     }
372 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:383:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
381 |                 Task { [weak self] in
382 |                     await MainActor.run {
383 |                         self?.refresh(reason: .unlock)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
384 |                     }
385 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:396:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
394 |                 Task { [weak self] in
395 |                     await MainActor.run {
396 |                         self?.refresh(reason: .dayChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
397 |                     }
398 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:409:25: warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
407 |                 Task { [weak self] in
408 |                     await MainActor.run {
409 |                         self?.refresh(reason: .clockChanged)
    |                         `- warning: reference to captured var 'self' in concurrently-executing code; this is an error in the Swift 6 language mode [#SendableClosureCaptures]
410 |                     }
411 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaView.swift:1082:29: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1080 |         for segment in parsed.segments {
1081 |             let slice = String(chars[segment.range])
1082 |             result = result + styledSlice(slice, kind: segment.kind, color: color)
     |                             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
1083 |         }
1084 |         return result.font(base).foregroundStyle(color)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:1460:32: warning: use '#selector' instead of explicitly constructing a 'Selector'
1458 |         }
1459 | 
1460 |         textView.doCommand(by: Selector(("deleteToBeginningOfLine:")))
     |                                `- warning: use '#selector' instead of explicitly constructing a 'Selector'
1461 |         return true
1462 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelController.swift:2108:42: warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2106 |         }
2107 |         if let textView = firstResponder as? NSTextView,
2108 |            let field = textView.delegate as? CapturePickerFilterNSTextField,
     |                                          `- warning: cast from '(any NSTextViewDelegate)?' to unrelated type 'CapturePickerFilterNSTextField' always fails
2109 |            field.accessibilityIdentifier() == identifier
2110 |         {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:41: warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                         `- warning: reference to property 'currentDraftHasTemplate' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:2468:67: warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2466 |                         requireInboxRouteChoice: true,
 2467 |                         inboxRouteCapabilityAdvertised: submitContext.inboxRouteCapabilityAdvertised,
 2468 |                         templateOrigin: currentDraftHasTemplate ? templateOrigin : nil
      |                                                                   `- warning: reference to property 'templateOrigin' in closure requires explicit use of 'self' to make capture semantics explicit; this is an error in the Swift 6 language mode
 2469 |                     )
 2470 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:8777:19: warning: variable 'current' was never mutated; consider changing to 'let' constant
 8775 |         newName: String
 8776 |     ) {
 8777 |         guard var current = relationLabelPrompt,
      |                   `- warning: variable 'current' was never mutated; consider changing to 'let' constant
 8778 |               let rename = current.rename,
 8779 |               current.draftSnapshot == draftSnapshot,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11839:23: warning: no 'async' operations occur within 'await' expression
11837 |                 }
11838 | 
11839 |                 guard await self?.isCurrentAnalysis(generation) == true else {
      |                       `- warning: no 'async' operations occur within 'await' expression
11840 |                     return
11841 |                 }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11844:21: warning: no 'async' operations occur within 'await' expression
11842 | 
11843 |                 if pickerNeeded == nil {
11844 |                     await self?.startLivePreview(
      |                     `- warning: no 'async' operations occur within 'await' expression
11845 |                         draft: draft,
11846 |                         previewDraft: closePending?.trimmed ?? draft,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11858:27: warning: no 'async' operations occur within 'await' expression
11856 |                     await completionGate.value
11857 |                     try Task.checkCancellation()
11858 |                     guard await self?.isCurrentAnalysis(generation) == true else {
      |                           `- warning: no 'async' operations occur within 'await' expression
11859 |                         return
11860 |                     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11865:20: warning: no 'async' operations occur within 'await' expression
11863 |                 if let cursorUTF8Offset,
11864 |                    requestCompletion,
11865 |                    await self?.shouldRequestCompletion(
      |                    `- warning: no 'async' operations occur within 'await' expression
11866 |                        parse: parse,
11867 |                        cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:11871:37: warning: no 'async' operations occur within 'await' expression
11869 |                    ) == true
11870 |                 {
11871 |                     if let cached = await self?.cachedRouteCompletion(
      |                                     `- warning: no 'async' operations occur within 'await' expression
11872 |                         parse: parse,
11873 |                         cursor: cursorUTF8Offset,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelModel.swift:12183:28: warning: no 'async' operations occur within 'await' expression
12181 |         Task { [weak self, processClient] in
12182 |             do {
12183 |                 let seed = await self?.activePriorityRollSeed() ?? UUID().uuidString
      |                            `- warning: no 'async' operations occur within 'await' expression
12184 |                 let processClientIdentity = processClient.identityToken
12185 |                 let preview = try await CaptureSignpost.measure("preview") {

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2477:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
2477 |             + Text(String(label[range.upperBound...]))
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2478 |     }
2479 | 

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:2476:13: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2474 |         }
2475 |         return Text(String(label[..<range.lowerBound]))
2476 |             + Text(String(label[range])).bold()
     |             `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
2477 |             + Text(String(label[range.upperBound...]))
2478 |     }

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3234:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3232 |                     + Text("●").foregroundStyle(
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3235 |                     .font(.caption)
3236 |                     .lineLimit(1)

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CapturePanelView.swift:3232:21: warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3230 |             if parts.count == 2 {
3231 |                 (Text(parts[0]).foregroundStyle(.secondary)
3232 |                     + Text("●").foregroundStyle(
     |                     `- warning: '+' was deprecated in macOS 26.0: Use string interpolation on `Text` instead: `Text("Hello \(name)")` [#DeprecatedDeclaration]
3233 |                         PomodoroHomeColor.color(for: hue, scheme: colorScheme))
3234 |                     + Text(parts[1]).foregroundStyle(.secondary))

[#DeprecatedDeclaration]: <https://docs.swift.org/compiler/documentation/diagnostics/deprecated-declaration>
[#SendableClosureCaptures]: <https://docs.swift.org/compiler/documentation/diagnostics/sendable-closure-captures>
[187/201] Compiling BobMacCapture HotKeyRegistry.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[188/201] Compiling BobMacCapture NotificationService.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[189/201] Compiling BobMacCapture PlainTextPaste.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[190/201] Compiling BobMacCapture PomodoroBlockView.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[191/201] Compiling BobMacCapture PomodoroHomeColor.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[192/201] Compiling BobMacCapture PomodoroNameField.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[193/201] Compiling BobMacCapture PomodoroThemeViews.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[194/201] Compiling BobMacCapture AXHighlightsTabsReader.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[195/201] Compiling BobMacCapture RefsActionsMenu.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[196/201] Compiling BobMacCapture RefsAnnotationImages.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[197/201] Compiling BobMacCapture RefsCodePreviewWell.swift
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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
[198/201] Emitting module BobMacCapture
/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:34: warning: call to main actor-isolated instance method 'activate()' in a synchronous nonisolated context [#ActorIsolatedCall]
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppDelegate.swift:1093:27: warning: main actor-isolated class property 'shared' can not be referenced from a nonisolated context
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/AppSettings.swift:271:52: warning: main actor-isolated static property 'refsHighlightsAppPathKey' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureAgendaStore.swift:80:70: warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 78 |         processClient: BobProcessClient? = nil,
 79 |         vaultRootPath: String = "",
 80 |         today: @Sendable @escaping () -> String = CaptureAgendaStore.localToday,
    |                                                                      `- warning: converting non-Sendable function value to '@Sendable () -> String' may introduce data races
 81 |         now: @Sendable @escaping () -> Date = { Date() },
 82 |         workspaceCenter: NotificationCenter? = nil,

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureShowRefreshWindow.swift:15:51: warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
13 | /// `RefsLibrary.pullThrottleInterval` so Capture and Refs use one constant.
14 | enum CaptureShowRefreshWindow {
15 |     static let pullThrottleInterval = RefsLibrary.pullThrottleInterval
   |                                                   `- warning: main actor-isolated static property 'pullThrottleInterval' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
16 | 
17 |     /// Show-triggered refreshes skip when the last spawn started inside

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsLibrary.swift:172:23: note: static property declared here
 170 | 
 171 |     /// Minimum seconds between panel-open pulls on the `refs-pull` lane.
 172 |     public static let pullThrottleInterval: TimeInterval = 5
     |                       `- note: static property declared here
 173 | 
 174 |     private var fetcher: RefsFetching?

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:9:42: warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
 7 | struct CaptureTargetsRefreshGate: Sendable {
 8 |     var lastStartedAt: Date?
 9 |     var now: @Sendable () -> Date = Date.init
   |                                          `- warning: converting non-Sendable function value to '@Sendable () -> Date' may introduce data races
10 | 
11 |     /// Returns true when the refresh should run, recording the start.

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsAnnotationImages.swift:188:34: warning: main actor-isolated static property 'defaultByteLimit' can not be referenced from a nonisolated context; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-wikilink-task.ogiMy2/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:156:21: warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
154 |                 .appendingPathComponent("org.bobs.bob-mac-capture/refs")
155 |         }
156 |         self.reader = reader ?? Self.readIntrinsics
    |                     `- warning: converting non-Sendable function value to '@Sendable (URL) async -> RefsPDFIntrinsics' may introduce data races
157 |     }
158 | 

[#ActorIsolatedCall]: <https://docs.swift.org/compiler/documentation/diagnostics/actor-isolated-call>
[198/201] Write Objects.LinkFileList
[199/201] Linking BobMacCapture
[200/201] Applying BobMacCapture
Build of product 'BobMacCapture' complete! (100.69s)
/tmp/bob-mac-capture-wikilink-task.ogiMy2/bundle/Bob Mac Capture.app/Contents/MacOS/BobMacCapture: replacing existing signature
/tmp/bob-mac-capture-wikilink-task.ogiMy2/bundle/Bob Mac Capture.app: replacing existing signature
/tmp/bob-mac-capture-wikilink-task.ogiMy2/bundle/Bob Mac Capture.app
./Scripts/typecheck-tests.sh
[0/1] Planning build
Building for debugging...
[0/11] Write sources
[2/13] Write refs-rank-entitlement.plist
[3/13] Write BobMacCaptureInstallHelper-entitlement.plist
[4/13] Write swift-version--1AB21518FC5DEDBE.txt
[6/18] Compiling BobMacCaptureInstallHelper BobMacCaptureInstallHelperMain.swift
[7/18] Compiling BobMacCaptureInstallHelper InstallHelperArguments.swift
[8/18] Emitting module refs_rank
[9/18] Compiling refs_rank main.swift
[10/18] Emitting module BobMacCaptureInstallHelper
[11/18] Compiling BobMacCaptureInstallHelper InstallRelauncher.swift
[12/18] Compiling BobMacCaptureInstallHelper InstallHelperError.swift
[12/18] Write Objects.LinkFileList
[14/18] Linking BobMacCaptureInstallHelper
[15/18] Applying BobMacCaptureInstallHelper
[16/18] Linking refs-rank
[17/18] Applying refs-rank
Build complete! (1.75s)
PASS BobMacCaptureTests
PASS BobMacCaptureInstallHelperTests
PASS CaptureCoreTests
PASS RefsCoreTests
Type-check only: macOS test targets were checked against a stub; CI still runs the tests.
/tmp/run-wikilink-task-mac-verification.sh: line 9: Scripts/macos-ci-check: No such file or directory
failed  exit=127  duration=116709ms

