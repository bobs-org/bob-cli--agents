# Chat History - ace-run (bob-cli-go.12--mon-0)

- **TIMESTAMP:** 2026-11-04 11:23:48 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-go.12--mon-0

## Prompt

sase monitor start --command 'set +e\nsource_dir=/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_29/sase/repos/linked/bob-mac-capture\nmac_scratch=\nathena_scratch=\ncleanup_remote() {\n  if [ -n "$mac_scratch" ]; then ssh -o ConnectTimeout=10 mac "python3 -c \'import shutil,sys; shutil.rmtree(sys.argv[1])\' \'$mac_scratch\'" >/dev/null 2>&1 || true; fi\n  if [ -n "$athena_scratch" ]; then ssh -o ConnectTimeout=10 athena "python3 -c \'import shutil,sys; shutil.rmtree(sys.argv[1])\' \'$athena_scratch\'" >/dev/null 2>&1 || true; fi\n}\ntrap cleanup_remote EXIT HUP INT TERM\nmac_setup=0\nmac_copy=125\nmac_bundle=125\nmac_typecheck=125\nmac_scratch=$(ssh -o ConnectTimeout=10 mac \'mktemp -d /tmp/bob-mac-capture-go12.XXXXXX\')\nmac_setup=$?\nif [ "$mac_setup" -eq 0 ]; then\n  rsync --archive --exclude=\'.build\' --exclude=\'.git\' "$source_dir"/ "mac:$mac_scratch"/\n  mac_copy=$?\n  if [ "$mac_copy" -eq 0 ]; then\n    ssh -o ConnectTimeout=10 mac "cd \'$mac_scratch\' && ./Scripts/bundle.sh --identity -"\n    mac_bundle=$?\n    ssh -o ConnectTimeout=10 mac "cd \'$mac_scratch\' && just typecheck-tests"\n    mac_typecheck=$?\n  fi\nfi\nathena_setup=0\nathena_copy=125\nathena_portable=125\nathena_scratch=$(ssh -o ConnectTimeout=10 athena \'mktemp -d /tmp/bob-mac-capture-go12.XXXXXX\')\nathena_setup=$?\nif [ "$athena_setup" -eq 0 ]; then\n  rsync --archive --exclude=\'.build\' --exclude=\'.git\' "$source_dir"/ "athena:$athena_scratch"/\n  athena_copy=$?\n  if [ "$athena_copy" -eq 0 ]; then\n    ssh -o ConnectTimeout=10 athena "cd \'$athena_scratch\' && just portable-check"\n    athena_portable=$?\n  fi\nfi\nprintf \'Mac: setup=%s copy=%s bundle=%s typecheck-tests=%s\\n\' "$mac_setup" "$mac_copy" "$mac_bundle" "$mac_typecheck"\nprintf \'Athena: setup=%s copy=%s portable-check=%s\\n\' "$athena_setup" "$athena_copy" "$athena_portable"\nif [ "$mac_setup" -ne 0 ] || [ "$mac_copy" -ne 0 ] || [ "$mac_bundle" -ne 0 ] || [ "$mac_typecheck" -ne 0 ] || [ "$athena_setup" -ne 0 ] || [ "$athena_copy" -ne 0 ] || [ "$athena_portable" -ne 0 ]; then exit 1; fi\nexit 0' --reason 'Run Mac and Athena checks on fresh Bob Mac Capture scratch copies'

## Response

sase tool run ac82e892d55d88a105d83e9129f6d829
Building for production...
[0/6] Write sources
[3/6] Write swift-version--1AB21518FC5DEDBE.txt
[5/7] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:8858:13: warning: no calls to throwing functions occur within 'try' expression
 8856 |         let container = try decoder.singleValueContainer()
 8857 |         // Explicit null has no value; treat it as absent.
 8858 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8859 |             throw DecodingError.valueNotFound(
 8860 |                 CaptureThemeSuggestion.self,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureTransferPresentation.swift:311:35: error: constant 'self.rows' captured by a closure before being initialized
309 |         let noun = count == 1 ? "task" : "tasks"
310 |         headerText = "⤵ Merges \(count) \(noun) into \(targetLabel)"
311 |         rows = capture.merges.map { merge in
    |                                   `- error: constant 'self.rows' captured by a closure before being initialized
312 |             let text = merge.message.isEmpty
313 |                 ? "\(merge.source.title ?? merge.source.blockID ?? "Task") → \(targetLabel)"
./Scripts/typecheck-tests.sh
Building for debugging...
[0/18] Write sources
[5/18] Write BobMacCaptureInstallHelper-entitlement.plist
[5/18] Write refs-rank-entitlement.plist
[5/18] Write BobMacCapture-entitlement.plist
[8/18] Write swift-version--1AB21518FC5DEDBE.txt
[10/98] Compiling CaptureCore CaptureTaskThemePresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureTransferPresentation.swift:311:35: error: constant 'self.rows' captured by a closure before being initialized
309 |         let noun = count == 1 ? "task" : "tasks"
310 |         headerText = "⤵ Merges \(count) \(noun) into \(targetLabel)"
311 |         rows = capture.merges.map { merge in
    |                                   `- error: constant 'self.rows' captured by a closure before being initialized
312 |             let text = merge.message.isEmpty
313 |                 ? "\(merge.source.title ?? merge.source.blockID ?? "Task") → \(targetLabel)"
[11/98] Compiling CaptureCore CaptureTaskTypeMenuPresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureTransferPresentation.swift:311:35: error: constant 'self.rows' captured by a closure before being initialized
309 |         let noun = count == 1 ? "task" : "tasks"
310 |         headerText = "⤵ Merges \(count) \(noun) into \(targetLabel)"
311 |         rows = capture.merges.map { merge in
    |                                   `- error: constant 'self.rows' captured by a closure before being initialized
312 |             let text = merge.message.isEmpty
313 |                 ? "\(merge.source.title ?? merge.source.blockID ?? "Task") → \(targetLabel)"
[12/98] Compiling CaptureCore CaptureTextRanges.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureTransferPresentation.swift:311:35: error: constant 'self.rows' captured by a closure before being initialized
309 |         let noun = count == 1 ? "task" : "tasks"
310 |         headerText = "⤵ Merges \(count) \(noun) into \(targetLabel)"
311 |         rows = capture.merges.map { merge in
    |                                   `- error: constant 'self.rows' captured by a closure before being initialized
312 |             let text = merge.message.isEmpty
313 |                 ? "\(merge.source.title ?? merge.source.blockID ?? "Task") → \(targetLabel)"
[13/98] Compiling CaptureCore CaptureTodayPomodoroGoto.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureTransferPresentation.swift:311:35: error: constant 'self.rows' captured by a closure before being initialized
309 |         let noun = count == 1 ? "task" : "tasks"
310 |         headerText = "⤵ Merges \(count) \(noun) into \(targetLabel)"
311 |         rows = capture.merges.map { merge in
    |                                   `- error: constant 'self.rows' captured by a closure before being initialized
312 |             let text = merge.message.isEmpty
313 |                 ? "\(merge.source.title ?? merge.source.blockID ?? "Task") → \(targetLabel)"
[14/98] Compiling CaptureCore CaptureTogglePresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureTransferPresentation.swift:311:35: error: constant 'self.rows' captured by a closure before being initialized
309 |         let noun = count == 1 ? "task" : "tasks"
310 |         headerText = "⤵ Merges \(count) \(noun) into \(targetLabel)"
311 |         rows = capture.merges.map { merge in
    |                                   `- error: constant 'self.rows' captured by a closure before being initialized
312 |             let text = merge.message.isEmpty
313 |                 ? "\(merge.source.title ?? merge.source.blockID ?? "Task") → \(targetLabel)"
[15/98] Compiling CaptureCore CaptureTransferPresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureTransferPresentation.swift:311:35: error: constant 'self.rows' captured by a closure before being initialized
309 |         let noun = count == 1 ? "task" : "tasks"
310 |         headerText = "⤵ Merges \(count) \(noun) into \(targetLabel)"
311 |         rows = capture.merges.map { merge in
    |                                   `- error: constant 'self.rows' captured by a closure before being initialized
312 |             let text = merge.message.isEmpty
313 |                 ? "\(merge.source.title ?? merge.source.blockID ?? "Task") → \(targetLabel)"
[16/98] Compiling CaptureCore CaptureUnconfiguredThemePresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureTransferPresentation.swift:311:35: error: constant 'self.rows' captured by a closure before being initialized
309 |         let noun = count == 1 ? "task" : "tasks"
310 |         headerText = "⤵ Merges \(count) \(noun) into \(targetLabel)"
311 |         rows = capture.merges.map { merge in
    |                                   `- error: constant 'self.rows' captured by a closure before being initialized
312 |             let text = merge.message.isEmpty
313 |                 ? "\(merge.source.title ?? merge.source.blockID ?? "Task") → \(targetLabel)"
[17/98] Compiling CaptureCore CompletionRowContent.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureTransferPresentation.swift:311:35: error: constant 'self.rows' captured by a closure before being initialized
309 |         let noun = count == 1 ? "task" : "tasks"
310 |         headerText = "⤵ Merges \(count) \(noun) into \(targetLabel)"
311 |         rows = capture.merges.map { merge in
    |                                   `- error: constant 'self.rows' captured by a closure before being initialized
312 |             let text = merge.message.isEmpty
313 |                 ? "\(merge.source.title ?? merge.source.blockID ?? "Task") → \(targetLabel)"
[18/98] Compiling CaptureCore DependencyPickerPresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureTransferPresentation.swift:311:35: error: constant 'self.rows' captured by a closure before being initialized
309 |         let noun = count == 1 ? "task" : "tasks"
310 |         headerText = "⤵ Merges \(count) \(noun) into \(targetLabel)"
311 |         rows = capture.merges.map { merge in
    |                                   `- error: constant 'self.rows' captured by a closure before being initialized
312 |             let text = merge.message.isEmpty
313 |                 ? "\(merge.source.title ?? merge.source.blockID ?? "Task") → \(targetLabel)"
[19/98] Compiling CaptureCore FuzzyMatcher.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureTransferPresentation.swift:311:35: error: constant 'self.rows' captured by a closure before being initialized
309 |         let noun = count == 1 ? "task" : "tasks"
310 |         headerText = "⤵ Merges \(count) \(noun) into \(targetLabel)"
311 |         rows = capture.merges.map { merge in
    |                                   `- error: constant 'self.rows' captured by a closure before being initialized
312 |             let text = merge.message.isEmpty
313 |                 ? "\(merge.source.title ?? merge.source.blockID ?? "Task") → \(targetLabel)"
[20/98] Compiling CaptureCore ObsidianOpenURL.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureTransferPresentation.swift:311:35: error: constant 'self.rows' captured by a closure before being initialized
309 |         let noun = count == 1 ? "task" : "tasks"
310 |         headerText = "⤵ Merges \(count) \(noun) into \(targetLabel)"
311 |         rows = capture.merges.map { merge in
    |                                   `- error: constant 'self.rows' captured by a closure before being initialized
312 |             let text = merge.message.isEmpty
313 |                 ? "\(merge.source.title ?? merge.source.blockID ?? "Task") → \(targetLabel)"
[21/98] Compiling CaptureCore CaptureRelationHeldPresentation.swift
[22/98] Compiling CaptureCore CaptureRelationSuccessorModels.swift
[23/98] Compiling CaptureCore CaptureRelationshipCopy.swift
[24/98] Compiling CaptureCore CaptureRelationshipPresentation.swift
[25/98] Compiling CaptureCore CaptureSavedTemplates.swift
[26/98] Compiling CaptureCore CaptureSubBulletPresentation.swift
[27/98] Compiling CaptureCore CaptureSuccessorOfferRows.swift
[28/98] Compiling CaptureCore CaptureSuccessorPresentation.swift
[29/98] Compiling CaptureCore CaptureTargetsCache.swift
[30/98] Compiling CaptureCore CaptureTaskBlockPresentation.swift
[31/98] Compiling CaptureCore CaptureTaskCompletePresentation.swift
[32/98] Compiling CaptureCore CapturePomodoroResetPresentation.swift
[33/98] Compiling CaptureCore CapturePomodoroShiftPresentation.swift
[34/98] Compiling CaptureCore CapturePomodoroSplitPresentation.swift
[35/98] Compiling CaptureCore CapturePomodoroStartPresentation.swift
[36/98] Compiling CaptureCore CaptureProjectNotePresentation.swift
[37/98] Compiling CaptureCore CaptureRefFileUnder.swift
[38/98] Compiling CaptureCore CaptureRefPresentation.swift
[39/98] Compiling CaptureCore CaptureRelatedModels.swift
[40/98] Compiling CaptureCore CaptureRelationCancelPresentation.swift
[41/98] Compiling CaptureCore CaptureRelationCloseEffect.swift
[42/98] Compiling CaptureCore CaptureRelationCompletePresentation.swift
[43/109] Compiling CaptureCore CaptureAgendaInlineText.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[44/109] Compiling CaptureCore CaptureAgendaLayout.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[45/109] Compiling CaptureCore CaptureAgendaModels.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[46/109] Compiling CaptureCore CaptureAgendaPresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[47/109] Compiling CaptureCore CaptureAgendaRefreshFilter.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[48/109] Compiling CaptureCore CaptureAgendaRefreshState.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[49/109] Compiling CaptureCore CaptureAgendaVisibility.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[50/109] Compiling CaptureCore CaptureBlockDiffRow.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[51/109] Compiling CaptureCore CaptureBlockIDSplice.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[52/109] Compiling CaptureCore CaptureClipPresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[53/109] Compiling CaptureCore CaptureCloseTaskCommaAssist.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[54/109] Compiling CaptureCore CaptureCloseTaskCommaProvenance.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[55/109] Compiling CaptureCore ParentTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[56/109] Compiling CaptureCore PomodoroHomes.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[57/109] Compiling CaptureCore ProjectTaskMovePickerPresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[58/109] Compiling CaptureCore SimilarTasksBandEdits.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[59/109] Compiling CaptureCore SimilarTasksBandPolicy.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[60/109] Compiling CaptureCore SimilarTasksBandPresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[61/109] Compiling CaptureCore TaskCompletePickerPresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[62/109] Compiling CaptureCore TaskDisplayText.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[63/109] Compiling CaptureCore TaskLinkPickerPresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[64/109] Compiling CaptureCore WikilinkTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[65/109] Compiling CaptureCore WorkBadgeTone.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[66/109] Emitting module CaptureCore
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[67/109] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[68/109] Compiling CaptureCore BlockIDPickerIndex.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[69/109] Compiling CaptureCore BlockIDRules.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[70/109] Compiling CaptureCore BobEnvironment.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[71/109] Compiling CaptureCore BobErrors.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[72/109] Compiling CaptureCore BobExecutableResolver.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[73/109] Compiling CaptureCore BobMacCaptureLaunchContext.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[74/109] Compiling CaptureCore BobProcessClient.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[75/109] Compiling CaptureCore CanceledDraftStashStore.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[76/109] Compiling CaptureCore CaptureAgendaBoundaryRefresh.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[77/109] Compiling CaptureCore CaptureAgendaFitPlanner.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[78/109] Compiling CaptureCore CaptureAgendaHold.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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

/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CanceledDraftStashStore.swift:46:17: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'FileCanceledDraftStashStore' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
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
[79/109] Compiling CaptureCore CaptureCompletionMenu.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:8858:13: warning: no calls to throwing functions occur within 'try' expression
 8856 |         let container = try decoder.singleValueContainer()
 8857 |         // Explicit null has no value; treat it as absent.
 8858 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8859 |             throw DecodingError.valueNotFound(
 8860 |                 CaptureThemeSuggestion.self,
[80/109] Compiling CaptureCore CaptureDrawerMenuPresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:8858:13: warning: no calls to throwing functions occur within 'try' expression
 8856 |         let container = try decoder.singleValueContainer()
 8857 |         // Explicit null has no value; treat it as absent.
 8858 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8859 |             throw DecodingError.valueNotFound(
 8860 |                 CaptureThemeSuggestion.self,
[81/109] Compiling CaptureCore CaptureEditWrite.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:8858:13: warning: no calls to throwing functions occur within 'try' expression
 8856 |         let container = try decoder.singleValueContainer()
 8857 |         // Explicit null has no value; treat it as absent.
 8858 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8859 |             throw DecodingError.valueNotFound(
 8860 |                 CaptureThemeSuggestion.self,
[82/109] Compiling CaptureCore CaptureGrammarGate.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:8858:13: warning: no calls to throwing functions occur within 'try' expression
 8856 |         let container = try decoder.singleValueContainer()
 8857 |         // Explicit null has no value; treat it as absent.
 8858 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8859 |             throw DecodingError.valueNotFound(
 8860 |                 CaptureThemeSuggestion.self,
[83/109] Compiling CaptureCore CaptureInboxRoutePresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:8858:13: warning: no calls to throwing functions occur within 'try' expression
 8856 |         let container = try decoder.singleValueContainer()
 8857 |         // Explicit null has no value; treat it as absent.
 8858 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8859 |             throw DecodingError.valueNotFound(
 8860 |                 CaptureThemeSuggestion.self,
[84/109] Compiling CaptureCore CaptureLineCaseToggle.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:8858:13: warning: no calls to throwing functions occur within 'try' expression
 8856 |         let container = try decoder.singleValueContainer()
 8857 |         // Explicit null has no value; treat it as absent.
 8858 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8859 |             throw DecodingError.valueNotFound(
 8860 |                 CaptureThemeSuggestion.self,
[85/109] Compiling CaptureCore CaptureLinkGuardPresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:8858:13: warning: no calls to throwing functions occur within 'try' expression
 8856 |         let container = try decoder.singleValueContainer()
 8857 |         // Explicit null has no value; treat it as absent.
 8858 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8859 |             throw DecodingError.valueNotFound(
 8860 |                 CaptureThemeSuggestion.self,
[86/109] Compiling CaptureCore CaptureList.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:8858:13: warning: no calls to throwing functions occur within 'try' expression
 8856 |         let container = try decoder.singleValueContainer()
 8857 |         // Explicit null has no value; treat it as absent.
 8858 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8859 |             throw DecodingError.valueNotFound(
 8860 |                 CaptureThemeSuggestion.self,
[87/109] Compiling CaptureCore CaptureModels.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:8858:13: warning: no calls to throwing functions occur within 'try' expression
 8856 |         let container = try decoder.singleValueContainer()
 8857 |         // Explicit null has no value; treat it as absent.
 8858 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8859 |             throw DecodingError.valueNotFound(
 8860 |                 CaptureThemeSuggestion.self,
[88/109] Compiling CaptureCore CaptureNotePullPresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:8858:13: warning: no calls to throwing functions occur within 'try' expression
 8856 |         let container = try decoder.singleValueContainer()
 8857 |         // Explicit null has no value; treat it as absent.
 8858 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8859 |             throw DecodingError.valueNotFound(
 8860 |                 CaptureThemeSuggestion.self,
[89/109] Compiling CaptureCore CaptureOpenHintPresentation.swift
/private/tmp/bob-mac-capture-go12.RSRhIc/Sources/CaptureCore/CaptureModels.swift:8858:13: warning: no calls to throwing functions occur within 'try' expression
 8856 |         let container = try decoder.singleValueContainer()
 8857 |         // Explicit null has no value; treat it as absent.
 8858 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8859 |             throw DecodingError.valueNotFound(
 8860 |                 CaptureThemeSuggestion.self,
[90/109] Compiling CaptureCore CaptureOpenPlan.swift
[91/109] Compiling CaptureCore CapturePanelPlacement.swift
[92/109] Compiling CaptureCore CapturePickerHelpers.swift
[93/109] Compiling CaptureCore CapturePickerPresentation.swift
[94/109] Compiling CaptureCore CapturePlanBudgetPresentation.swift
[95/109] Compiling CaptureCore CapturePomodoroAdjustPresentation.swift
[96/109] Compiling CaptureCore CapturePomodoroBlockPresentation.swift
[97/109] Compiling CaptureCore CapturePomodoroClosePresentation.swift
[98/109] Compiling CaptureCore CapturePomodoroLineTokens.swift
[99/109] Compiling CaptureCore CapturePomodoroLinkPresentation.swift
[100/109] Compiling CaptureCore CapturePomodoroMergePresentation.swift
error: recipe `typecheck-tests` failed on line 30 with exit code 1
if command -v swift-format >/dev/null 2>&1; then swift-format lint --recursive Package.swift Sources Tests; else swift format lint --recursive Package.swift Sources Tests; fi
/home/bryan/.local/share/funky/funky.sh: line 29: XDG_DATA_HOME: unbound variable
Package.swift:8:1: warning: [Indentation] replace leading whitespace with 4 spaces
Package.swift:9:1: warning: [Indentation] indent by 4 spaces
Package.swift:10:1: warning: [Indentation] indent by 4 spaces
Package.swift:11:1: warning: [Indentation] indent by 4 spaces
Package.swift:12:1: warning: [Indentation] indent by 4 spaces
Package.swift:13:1: warning: [Indentation] indent by 4 spaces
Package.swift:14:1: warning: [Indentation] indent by 4 spaces
Package.swift:15:1: warning: [Indentation] indent by 4 spaces
Package.swift:16:1: warning: [Indentation] indent by 4 spaces
Package.swift:17:1: warning: [Indentation] replace leading whitespace with 4 spaces
Package.swift:18:1: warning: [Indentation] replace leading whitespace with 4 spaces
Package.swift:19:1: warning: [Indentation] indent by 4 spaces
Package.swift:20:1: warning: [Indentation] indent by 4 spaces
Package.swift:21:1: warning: [Indentation] indent by 4 spaces
Package.swift:22:1: warning: [Indentation] indent by 4 spaces
Package.swift:23:1: warning: [Indentation] indent by 4 spaces
Package.swift:24:1: warning: [Indentation] indent by 4 spaces
Package.swift:25:1: warning: [Indentation] indent by 4 spaces
Package.swift:26:1: warning: [Indentation] indent by 4 spaces
Package.swift:27:1: warning: [Indentation] indent by 4 spaces
Package.swift:28:1: warning: [Indentation] indent by 4 spaces
Package.swift:29:1: warning: [Indentation] indent by 4 spaces
Package.swift:30:1: warning: [Indentation] indent by 4 spaces
Package.swift:31:1: warning: [Indentation] indent by 4 spaces
Package.swift:32:1: warning: [Indentation] indent by 4 spaces
Package.swift:33:1: warning: [Indentation] indent by 4 spaces
Package.swift:34:1: warning: [Indentation] indent by 4 spaces
Package.swift:35:1: warning: [Indentation] indent by 4 spaces
Package.swift:36:1: warning: [Indentation] indent by 4 spaces
Package.swift:37:1: warning: [Indentation] indent by 4 spaces
Package.swift:38:1: warning: [Indentation] indent by 4 spaces
Package.swift:39:1: warning: [Indentation] indent by 4 spaces
Package.swift:40:1: warning: [Indentation] indent by 4 spaces
Package.swift:41:1: warning: [Indentation] indent by 4 spaces
Package.swift:42:1: warning: [Indentation] indent by 4 spaces
Package.swift:43:1: warning: [Indentation] indent by 4 spaces
Package.swift:44:1: warning: [Indentation] indent by 4 spaces
Package.swift:45:1: warning: [Indentation] indent by 4 spaces
Package.swift:46:1: warning: [Indentation] indent by 4 spaces
Package.swift:47:1: warning: [Indentation] replace leading whitespace with 4 spaces
Package.swift:49:1: warning: [Indentation] replace leading whitespace with 4 spaces
Package.swift:50:1: warning: [Indentation] replace leading whitespace with 4 spaces
Sources/refs-rank/main.swift:246:20: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsTodayLinkPresentation.swift:94:1: warning: [LineLength] line is too long
Sources/RefsCore/RefsTodayLinkPresentation.swift:170:1: warning: [LineLength] line is too long
Sources/RefsCore/RefsTodayLinkPresentation.swift:173:94: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsTodayLinkPresentation.swift:174:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsTodayLinkPresentation.swift:188:1: warning: [LineLength] line is too long
Sources/RefsCore/RefsTodayLinkPresentation.swift:227:100: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsTodayLinkPresentation.swift:231:1: warning: [LineLength] line is too long
Sources/RefsCore/RefsTodayLinkPresentation.swift:273:1: warning: [LineLength] line is too long
Sources/RefsCore/RefsTodayLinkPresentation.swift:274:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsTodayLinkPresentation.swift:296:97: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsTodayLinkCard.swift:164:1: warning: [LineLength] line is too long
Sources/RefsCore/RefsTodayLinkCard.swift:200:100: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsTodayLinkCard.swift:330:20: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsToday.swift:96:18: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsToday.swift:97:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsToday.swift:98:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsToday.swift:99:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsToday.swift:100:22: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsToday.swift:101:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsToday.swift:102:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsToday.swift:103:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsTabsRanking.swift:143:22: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsTabsRanking.swift:40:1: warning: [LineLength] line is too long
Sources/RefsCore/RefsTabsRanking.swift:59:1: warning: [LineLength] line is too long
Sources/RefsCore/RefsSectionedWindow.swift:43:29: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsSectionedWindow.swift:46:32: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsSectionedWindow.swift:68:1: warning: [Indentation] indent by 1 spaces
Sources/RefsCore/RefsSectionedWindow.swift:69:1: warning: [Indentation] indent by 1 spaces
Sources/RefsCore/RefsSectionedWindow.swift:76:1: warning: [Indentation] indent by 1 spaces
Sources/RefsCore/RefsSectionedWindow.swift:77:1: warning: [Indentation] indent by 1 spaces
Sources/RefsCore/RefsSectionedWindow.swift:132:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsSectionedWindow.swift:133:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsSectionedWindow.swift:177:19: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsSectionedWindow.swift:199:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsScan.swift:72:18: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsScan.swift:76:1: warning: [LineLength] line is too long
Sources/RefsCore/RefsScan.swift:266:1: warning: [LineLength] line is too long
Sources/RefsCore/RefsScan.swift:596:1: warning: [LineLength] line is too long
Sources/RefsCore/RefsScan.swift:597:41: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsRanking.swift:788:14: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsRanking.swift:790:14: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsRanking.swift:792:14: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsRanking.swift:950:26: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsRanking.swift:984:26: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsRanking.swift:992:26: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsRanking.swift:1019:26: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsRanking.swift:1033:14: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsRanking.swift:1050:14: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsRanking.swift:1085:14: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsRanking.swift:1151:18: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsRanking.swift:1258:18: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsRanking.swift:1260:18: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsRanking.swift:1262:18: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsRanking.swift:1886:41: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsRanking.swift:858:22: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsRanking.swift:859:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsRanking.swift:860:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsRanking.swift:860:18: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsPanelGeometry.swift:3:1: warning: [Indentation] replace leading whitespace with 4 spaces
Sources/RefsCore/RefsNewest.swift:58:14: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsNewest.swift:63:18: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsModel.swift:15:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsModel.swift:16:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsModel.swift:17:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsModel.swift:18:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsModel.swift:19:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsModel.swift:20:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsModel.swift:21:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsModel.swift:22:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsModel.swift:132:19: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsModel.swift:522:15: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsModel.swift:622:21: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsModel.swift:623:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsModel.swift:624:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsModel.swift:625:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsListScroll.swift:3:1: warning: [Indentation] replace leading whitespace with 4 spaces
Sources/RefsCore/RefsLinks.swift:87:18: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsLinks.swift:92:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsLinks.swift:93:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsLinks.swift:251:20: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsLinks.swift:296:31: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsLinks.swift:419:15: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsLinks.swift:474:27: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspectorImages.swift:3:1: warning: [Indentation] replace leading whitespace with 4 spaces
Sources/RefsCore/RefsInspectorImages.swift:62:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsInspectorImages.swift:63:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsInspectorImages.swift:64:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsInspectorImages.swift:86:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsInspectorImages.swift:87:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsInspectorImages.swift:106:21: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:29:19: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:30:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:31:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:32:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:154:30: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:155:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:156:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:157:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:161:22: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:162:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:163:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:164:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:165:16: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:166:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:167:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:168:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:279:32: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:280:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:281:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:282:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:386:32: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:387:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:388:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:389:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:391:28: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:392:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:393:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:394:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:420:26: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:421:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:422:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:470:24: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:471:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:472:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:472:18: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:482:27: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:483:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:484:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:484:18: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:531:14: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:532:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:533:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:533:24: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:554:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsInspector.swift:562:1: warning: [Indentation] unindent by 6 spaces
Sources/RefsCore/RefsInspector.swift:614:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsInspector.swift:615:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsInspector.swift:676:35: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:909:26: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:910:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:911:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:990:18: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:991:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:992:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:992:14: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:1100:48: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:1101:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:1102:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:1102:22: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:1125:26: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:1137:27: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsInspector.swift:1138:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:1139:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:1140:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:1141:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:1142:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:1143:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:1144:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsInspector.swift:1858:24: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsHighlightsTabs.swift:200:1: warning: [NoAccessLevelOnExtensionDeclaration] move this 'public' access modifier to precede each member inside this extension
Sources/RefsCore/RefsHighlightsTabs.swift:203:5: note: add 'public' access modifier to this declaration
Sources/RefsCore/RefsHighlightsTabs.swift:209:5: note: add 'public' access modifier to this declaration
Sources/RefsCore/RefsHighlightsTabs.swift:534:17: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsHighlightsTabs.swift:546:20: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsHighlightsTabs.swift:573:14: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsHighlightsTabs.swift:592:14: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/RefsHighlightsTabs.swift:77:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsHighlightsTabs.swift:78:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsHighlightsTabs.swift:79:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsHighlightsTabs.swift:80:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsHighlightsTabs.swift:91:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsHighlightsTabs.swift:92:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsHighlightsTabs.swift:301:28: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsHighlightsTabs.swift:315:1: warning: [Indentation] indent by 1 spaces
Sources/RefsCore/RefsHighlightsTabs.swift:402:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsHighlightsTabs.swift:421:25: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsHighlightsTabs.swift:570:101: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsHighlightsTabs.swift:608:2: warning: [RemoveLine] remove line break
Sources/RefsCore/RefsHighlightPicker.swift:24:1: warning: [LineLength] line is too long
Sources/RefsCore/RefsHighlightPicker.swift:43:35: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsFetching.swift:29:1: warning: [NoAccessLevelOnExtensionDeclaration] move this 'public' access modifier to precede each member inside this extension
Sources/RefsCore/RefsFetching.swift:33:5: note: add 'public' access modifier to this declaration
Sources/RefsCore/RefsFetching.swift:40:5: note: add 'public' access modifier to this declaration
Sources/RefsCore/RefsFetching.swift:47:5: note: add 'public' access modifier to this declaration
Sources/RefsCore/RefsFetching.swift:56:5: note: add 'public' access modifier to this declaration
Sources/RefsCore/RefsDecoding.swift:381:21: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsDecoding.swift:382:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsDecoding.swift:383:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsDecoding.swift:384:1: warning: [Indentation] indent by 4 spaces
/tmp/bob-mac-capture-go12.BHqRrC/Sources/RefsCore/RefsCopy.swift:822:95: warning: [TrailingComma] add trailing comma to the last element in multiline collection literal
Sources/RefsCore/RefsCopy.swift:275:26: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:276:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:277:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:278:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:279:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:280:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:281:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:282:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:283:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:284:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:285:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:286:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:288:22: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:289:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:290:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:291:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:292:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:293:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:294:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:295:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:296:22: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:297:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:298:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:299:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:300:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:301:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:302:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:303:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:304:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:305:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:306:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:307:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:308:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:309:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:310:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:314:26: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:315:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:316:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:317:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:318:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:319:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:320:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:321:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:322:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:323:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:324:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:325:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:326:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:328:30: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:329:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:330:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:331:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:332:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:333:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:334:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:335:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:339:26: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:340:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:341:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:342:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:343:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:344:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:345:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:348:26: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:349:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:350:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:351:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:352:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:353:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:354:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:357:22: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:358:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:359:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:360:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:361:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:362:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:363:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:364:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:365:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:366:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:367:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:368:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:369:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:370:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:371:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:372:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:373:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:374:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:385:26: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:386:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:387:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:388:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:389:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:390:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:391:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:392:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:393:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:394:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:395:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:396:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:397:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:398:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:399:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:400:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:401:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:402:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:403:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:406:30: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:407:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:408:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:409:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:410:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:411:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:412:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:413:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:414:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:415:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:416:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:417:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:418:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:419:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:420:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:421:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:422:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:423:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:427:26: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:428:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:429:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:430:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:431:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:432:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:433:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:434:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:437:26: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:438:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:439:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:440:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:441:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:442:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:443:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:445:22: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:446:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:447:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:448:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:449:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:450:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:451:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:459:30: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:460:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:461:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:462:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:463:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:464:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:465:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:466:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:467:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:468:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:469:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:470:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:486:30: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:487:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:488:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:489:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:490:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:491:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:492:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:493:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:494:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:499:30: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:500:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:501:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:502:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:503:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:504:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:505:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:506:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:507:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:739:30: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:775:19: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:776:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:777:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:779:1: warning: [LineLength] line is too long
Sources/RefsCore/RefsCopy.swift:803:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsCopy.swift:804:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsCopy.swift:806:1: warning: [LineLength] line is too long
Sources/RefsCore/RefsCopy.swift:972:26: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:973:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:974:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:996:31: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:997:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:998:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCopy.swift:1093:27: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:1097:25: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:1157:26: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:1179:26: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:1294:41: warning: [Spacing] add 1 space
Sources/RefsCore/RefsCopy.swift:1295:42: warning: [Spacing] add 1 space
Sources/RefsCore/RefsCopy.swift:1300:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsCopy.swift:1301:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsCopy.swift:1301:41: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:1309:27: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:1312:1: warning: [Indentation] indent by 1 spaces
Sources/RefsCore/RefsCopy.swift:1312:59: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:1326:19: warning: [Spacing] add 1 space
Sources/RefsCore/RefsCopy.swift:1327:19: warning: [Spacing] add 1 space
Sources/RefsCore/RefsCopy.swift:1328:19: warning: [Spacing] add 1 space
Sources/RefsCore/RefsCopy.swift:1329:19: warning: [Spacing] add 1 space
Sources/RefsCore/RefsCopy.swift:1330:19: warning: [Spacing] add 1 space
Sources/RefsCore/RefsCopy.swift:1331:19: warning: [Spacing] add 1 space
Sources/RefsCore/RefsCopy.swift:1332:19: warning: [Spacing] add 1 space
Sources/RefsCore/RefsCopy.swift:1333:19: warning: [Spacing] add 1 space
Sources/RefsCore/RefsCopy.swift:1334:19: warning: [Spacing] add 1 space
Sources/RefsCore/RefsCopy.swift:1546:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsCopy.swift:1547:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsCopy.swift:1565:21: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:1573:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsCopy.swift:1574:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsCopy.swift:1592:21: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:1752:22: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:1879:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsCopy.swift:1880:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsCopy.swift:1881:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsCopy.swift:1883:25: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:2017:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsCopy.swift:2018:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsCopy.swift:2019:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsCopy.swift:2021:25: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCopy.swift:2183:1: warning: [Indentation] unindent by 2 spaces
Sources/RefsCore/RefsCode.swift:135:1: warning: [LineLength] line is too long
Sources/RefsCore/RefsCode.swift:165:1: warning: [LineLength] line is too long
Sources/RefsCore/RefsCode.swift:166:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/RefsCode.swift:212:20: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCode.swift:479:19: warning: [AddLines] add 1 line break
Sources/RefsCore/RefsCode.swift:488:2: warning: [RemoveLine] remove line break
Sources/RefsCore/RefsCaption.swift:374:17: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/RefsCore/HighlightsSaveScan.swift:89:21: warning: [AddLines] add 1 line break
Sources/RefsCore/HighlightsSaveScan.swift:90:1: warning: [Indentation] indent by 4 spaces
Sources/RefsCore/HighlightsSaveScan.swift:91:1: warning: [Indentation] indent by 4 spaces
/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/TaskLinkPickerPresentation.swift:387:95: warning: [TrailingComma] add trailing comma to the last element in multiline collection literal
Sources/CaptureCore/TaskLinkPickerPresentation.swift:81:1: warning: [LineLength] line is too long
Sources/CaptureCore/TaskLinkPickerPresentation.swift:169:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/TaskLinkPickerPresentation.swift:170:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:171:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:172:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:173:1: warning: [LineLength] line is too long
Sources/CaptureCore/TaskLinkPickerPresentation.swift:173:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:174:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:175:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:176:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:177:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:180:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/TaskLinkPickerPresentation.swift:181:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:182:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:183:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:184:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:185:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:188:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/TaskLinkPickerPresentation.swift:189:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:190:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:191:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:192:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:193:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:196:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/TaskLinkPickerPresentation.swift:197:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:198:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:199:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:200:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:201:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:202:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:349:1: warning: [LineLength] line is too long
Sources/CaptureCore/TaskLinkPickerPresentation.swift:369:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:370:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:371:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:372:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:391:1: warning: [LineLength] line is too long
Sources/CaptureCore/TaskLinkPickerPresentation.swift:394:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:395:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:396:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:397:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:398:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:399:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:539:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/TaskLinkPickerPresentation.swift:571:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/TaskDisplayText.swift:58:30: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/CaptureCore/TaskDisplayText.swift:59:16: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/CaptureCore/TaskDisplayText.swift:70:41: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/CaptureCore/TaskDisplayText.swift:58:30: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/CaptureCore/TaskDisplayText.swift:59:16: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/CaptureCore/TaskDisplayText.swift:70:41: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/CaptureCore/TaskDisplayText.swift:58:30: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/CaptureCore/TaskDisplayText.swift:59:16: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/CaptureCore/TaskDisplayText.swift:70:41: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/CaptureCore/TaskDisplayText.swift:70:41: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/CaptureCore/TaskDisplayText.swift:59:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/TaskDisplayText.swift:179:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/TaskDisplayText.swift:180:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:28:1: warning: [LineLength] line is too long
Sources/CaptureCore/TaskCompletePickerPresentation.swift:70:1: warning: [LineLength] line is too long
Sources/CaptureCore/TaskCompletePickerPresentation.swift:98:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/TaskCompletePickerPresentation.swift:99:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:100:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:101:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:102:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:103:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:106:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/TaskCompletePickerPresentation.swift:107:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:108:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:109:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:110:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:111:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:192:1: warning: [LineLength] line is too long
Sources/CaptureCore/TaskCompletePickerPresentation.swift:193:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/TaskCompletePickerPresentation.swift:194:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:195:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:196:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:197:1: warning: [LineLength] line is too long
Sources/CaptureCore/TaskCompletePickerPresentation.swift:197:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:198:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:199:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:200:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:201:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:202:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:205:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/TaskCompletePickerPresentation.swift:206:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:207:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:208:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:209:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:210:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:213:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/TaskCompletePickerPresentation.swift:214:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:215:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:216:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:217:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:218:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:221:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/TaskCompletePickerPresentation.swift:222:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:223:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:224:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:225:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:226:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:229:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/TaskCompletePickerPresentation.swift:230:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:231:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:232:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:233:1: warning: [LineLength] line is too long
Sources/CaptureCore/TaskCompletePickerPresentation.swift:233:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:234:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/TaskCompletePickerPresentation.swift:241:1: warning: [LineLength] line is too long
Sources/CaptureCore/TaskCompletePickerPresentation.swift:465:1: warning: [LineLength] line is too long
Sources/CaptureCore/TaskCompletePickerPresentation.swift:622:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/SimilarTasksBandPresentation.swift:52:1: warning: [Indentation] unindent by 8 spaces
Sources/CaptureCore/SimilarTasksBandPresentation.swift:239:1: warning: [LineLength] line is too long
Sources/CaptureCore/SimilarTasksBandPresentation.swift:266:1: warning: [LineLength] line is too long
Sources/CaptureCore/SimilarTasksBandPolicy.swift:152:1: warning: [LineLength] line is too long
Sources/CaptureCore/SimilarTasksBandPolicy.swift:153:1: warning: [LineLength] line is too long
Sources/CaptureCore/SimilarTasksBandPolicy.swift:175:1: warning: [Indentation] unindent by 8 spaces
Sources/CaptureCore/SimilarTasksBandPolicy.swift:176:1: warning: [Indentation] unindent by 8 spaces
Sources/CaptureCore/SimilarTasksBandPolicy.swift:226:1: warning: [Indentation] unindent by 8 spaces
Sources/CaptureCore/SimilarTasksBandPolicy.swift:227:1: warning: [Indentation] unindent by 8 spaces
Sources/CaptureCore/SimilarTasksBandPolicy.swift:251:1: warning: [Indentation] unindent by 8 spaces
Sources/CaptureCore/SimilarTasksBandPolicy.swift:258:14: warning: [AddLines] add 1 line break
Sources/CaptureCore/SimilarTasksBandPolicy.swift:258:33: warning: [AddLines] add 1 line break
Sources/CaptureCore/SimilarTasksBandPolicy.swift:259:1: warning: [Indentation] indent by 8 spaces
Sources/CaptureCore/SimilarTasksBandPolicy.swift:260:1: warning: [Indentation] indent by 8 spaces
Sources/CaptureCore/SimilarTasksBandPolicy.swift:260:11: warning: [AddLines] add 1 line break
Sources/CaptureCore/SimilarTasksBandEdits.swift:59:1: warning: [LineLength] line is too long
Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:23:1: warning: [LineLength] line is too long
Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:318:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:347:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/PomodoroHomes.swift:37:16: warning: [AddLines] add 1 line break
Sources/CaptureCore/PomodoroHomes.swift:38:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/PomodoroHomes.swift:39:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/PomodoroHomes.swift:40:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/PomodoroHomes.swift:41:15: warning: [AddLines] add 1 line break
Sources/CaptureCore/PomodoroHomes.swift:42:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/PomodoroHomes.swift:43:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/PomodoroHomes.swift:44:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/PomodoroHomes.swift:48:16: warning: [AddLines] add 1 line break
Sources/CaptureCore/PomodoroHomes.swift:49:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/PomodoroHomes.swift:50:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/PomodoroHomes.swift:51:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/PomodoroHomes.swift:52:19: warning: [AddLines] add 1 line break
Sources/CaptureCore/PomodoroHomes.swift:117:15: warning: [AddLines] add 1 line break
Sources/CaptureCore/PomodoroHomes.swift:118:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/PomodoroHomes.swift:119:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/PomodoroHomes.swift:120:1: warning: [Indentation] indent by 4 spaces
/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/ParentTaskPickerPresentation.swift:301:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Sources/CaptureCore/ParentTaskPickerPresentation.swift:160:1: warning: [LineLength] line is too long
Sources/CaptureCore/ParentTaskPickerPresentation.swift:200:1: warning: [LineLength] line is too long
Sources/CaptureCore/ParentTaskPickerPresentation.swift:282:1: warning: [LineLength] line is too long
Sources/CaptureCore/ParentTaskPickerPresentation.swift:351:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/ParentTaskPickerPresentation.swift:352:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:353:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:354:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:355:1: warning: [LineLength] line is too long
Sources/CaptureCore/ParentTaskPickerPresentation.swift:355:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:356:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:357:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:358:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:359:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:362:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/ParentTaskPickerPresentation.swift:363:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:364:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:365:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:366:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:367:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:370:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/ParentTaskPickerPresentation.swift:371:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:372:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:373:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:374:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:375:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:378:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/ParentTaskPickerPresentation.swift:379:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:380:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:381:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:382:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:383:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:384:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:637:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/ParentTaskPickerPresentation.swift:671:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/ObsidianOpenURL.swift:81:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/ObsidianOpenURL.swift:82:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/ObsidianOpenURL.swift:83:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/ObsidianOpenURL.swift:84:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/ObsidianOpenURL.swift:94:25: warning: [AddLines] add 1 line break
Sources/CaptureCore/ObsidianOpenURL.swift:95:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ObsidianOpenURL.swift:96:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ObsidianOpenURL.swift:97:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ObsidianOpenURL.swift:98:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ObsidianOpenURL.swift:99:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ObsidianOpenURL.swift:105:31: warning: [AddLines] add 1 line break
Sources/CaptureCore/FuzzyMatcher.swift:146:1: warning: [LineLength] line is too long
Sources/CaptureCore/DependencyPickerPresentation.swift:92:1: warning: [LineLength] line is too long
Sources/CaptureCore/DependencyPickerPresentation.swift:126:1: warning: [LineLength] line is too long
Sources/CaptureCore/DependencyPickerPresentation.swift:201:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/DependencyPickerPresentation.swift:202:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:203:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:204:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:205:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:206:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:209:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/DependencyPickerPresentation.swift:210:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:211:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:212:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:213:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:214:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:217:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/DependencyPickerPresentation.swift:218:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:219:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:220:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:221:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:222:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:225:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/DependencyPickerPresentation.swift:226:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:227:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:228:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:229:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:230:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:233:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/DependencyPickerPresentation.swift:234:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:235:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:236:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:237:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:238:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:239:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/DependencyPickerPresentation.swift:355:24: warning: [AddLines] add 1 line break
Sources/CaptureCore/DependencyPickerPresentation.swift:407:1: warning: [LineLength] line is too long
Sources/CaptureCore/DependencyPickerPresentation.swift:643:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CompletionRowContent.swift:69:1: warning: [Indentation] unindent by 1 spaces
Sources/CaptureCore/CompletionRowContent.swift:70:1: warning: [Indentation] unindent by 1 spaces
Sources/CaptureCore/CompletionRowContent.swift:77:1: warning: [Indentation] unindent by 1 spaces
Sources/CaptureCore/CompletionRowContent.swift:78:1: warning: [Indentation] unindent by 1 spaces
Sources/CaptureCore/CompletionRowContent.swift:142:1: warning: [Indentation] unindent by 1 spaces
Sources/CaptureCore/CompletionRowContent.swift:330:1: warning: [Indentation] indent by 2 spaces
Sources/CaptureCore/CompletionRowContent.swift:331:1: warning: [Indentation] indent by 2 spaces
Sources/CaptureCore/CompletionRowContent.swift:332:1: warning: [Indentation] indent by 2 spaces
Sources/CaptureCore/CompletionRowContent.swift:333:1: warning: [Indentation] indent by 2 spaces
Sources/CaptureCore/CompletionRowContent.swift:334:1: warning: [Indentation] indent by 2 spaces
Sources/CaptureCore/CompletionRowContent.swift:505:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CompletionRowContent.swift:576:28: warning: [AddLines] add 1 line break
Sources/CaptureCore/CompletionRowContent.swift:587:1: warning: [LineLength] line is too long
Sources/CaptureCore/CompletionRowContent.swift:617:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CompletionRowContent.swift:634:32: warning: [AddLines] add 1 line break
Sources/CaptureCore/CompletionRowContent.swift:660:1: warning: [LineLength] line is too long
Sources/CaptureCore/CompletionRowContent.swift:847:28: warning: [AddLines] add 1 line break
Sources/CaptureCore/CompletionRowContent.swift:906:1: warning: [LineLength] line is too long
Sources/CaptureCore/CompletionRowContent.swift:964:1: warning: [LineLength] line is too long
Sources/CaptureCore/CompletionRowContent.swift:986:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CompletionRowContent.swift:1019:32: warning: [AddLines] add 1 line break
Sources/CaptureCore/CompletionRowContent.swift:1048:23: warning: [AddLines] add 1 line break
Sources/CaptureCore/CompletionRowContent.swift:1052:24: warning: [AddLines] add 1 line break
Sources/CaptureCore/CompletionRowContent.swift:1069:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CompletionRowContent.swift:1070:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CompletionRowContent.swift:1082:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/CompletionRowContent.swift:1128:36: warning: [AddLines] add 1 line break
Sources/CaptureCore/CompletionRowContent.swift:1182:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CompletionRowContent.swift:1183:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CompletionRowContent.swift:1184:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CompletionRowContent.swift:1216:1: warning: [LineLength] line is too long
Sources/CaptureCore/CompletionRowContent.swift:1244:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CompletionRowContent.swift:1327:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureTransferPresentation.swift:146:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureTransferPresentation.swift:148:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureTransferPresentation.swift:256:1: warning: [Indentation] unindent by 4 spaces
Sources/CaptureCore/CaptureTransferPresentation.swift:312:23: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureTogglePresentation.swift:252:19: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/CaptureCore/CaptureTogglePresentation.swift:252:19: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/CaptureCore/CaptureTogglePresentation.swift:252:19: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/CaptureCore/CaptureTogglePresentation.swift:444:12: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/CaptureCore/CaptureTogglePresentation.swift:444:12: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/CaptureCore/CaptureTogglePresentation.swift:89:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureTogglePresentation.swift:110:28: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureTogglePresentation.swift:136:35: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureTogglePresentation.swift:164:31: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureTogglePresentation.swift:191:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureTogglePresentation.swift:210:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureTogglePresentation.swift:252:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureTogglePresentation.swift:257:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureTogglePresentation.swift:426:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureTogglePresentation.swift:445:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CaptureTogglePresentation.swift:456:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureTogglePresentation.swift:457:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureTogglePresentation.swift:492:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CaptureTogglePresentation.swift:493:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CaptureTogglePresentation.swift:524:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureTogglePresentation.swift:529:32: warning: [Spacing] remove 1 space
Sources/CaptureCore/CaptureTogglePresentation.swift:529:36: warning: [Spacing] remove 1 space
Sources/CaptureCore/CaptureTogglePresentation.swift:529:63: warning: [Spacing] remove 1 space
Sources/CaptureCore/CaptureTogglePresentation.swift:529:67: warning: [Spacing] remove 1 space
Sources/CaptureCore/CaptureTogglePresentation.swift:534:19: warning: [Spacing] remove 1 space
Sources/CaptureCore/CaptureTogglePresentation.swift:534:23: warning: [Spacing] remove 1 space
Sources/CaptureCore/CaptureTaskCompletePresentation.swift:79:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureTaskBlockPresentation.swift:92:27: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureTaskBlockPresentation.swift:152:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureTaskBlockPresentation.swift:260:31: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureSuccessorPresentation.swift:211:46: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureSuccessorPresentation.swift:212:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureSuccessorPresentation.swift:213:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureSuccessorPresentation.swift:214:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureSuccessorPresentation.swift:215:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureSuccessorPresentation.swift:216:34: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureSuccessorPresentation.swift:229:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CaptureSuccessorPresentation.swift:230:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CaptureSuccessorPresentation.swift:231:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CaptureSuccessorPresentation.swift:232:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CaptureSuccessorPresentation.swift:345:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CaptureSuccessorPresentation.swift:346:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CaptureSuccessorOfferRows.swift:64:25: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureSavedTemplates.swift:147:95: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureSavedTemplates.swift:188:95: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureSavedTemplates.swift:189:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureSavedTemplates.swift:308:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureSavedTemplates.swift:317:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureSavedTemplates.swift:320:93: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureSavedTemplates.swift:406:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRelationshipPresentation.swift:134:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRelationshipPresentation.swift:138:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRelationshipPresentation.swift:188:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRelationshipPresentation.swift:312:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRelationshipPresentation.swift:332:20: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureRelationshipPresentation.swift:387:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRelationshipPresentation.swift:395:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRelationshipCopy.swift:134:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRelationshipCopy.swift:149:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRelationshipCopy.swift:187:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRelationSuccessorModels.swift:36:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRelationSuccessorModels.swift:294:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRelationSuccessorModels.swift:296:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRelationHeldPresentation.swift:16:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CaptureRelationHeldPresentation.swift:17:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CaptureRelationHeldPresentation.swift:18:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CaptureRelationHeldPresentation.swift:19:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CaptureRelationHeldPresentation.swift:20:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CaptureRelationHeldPresentation.swift:48:101: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureRelatedModels.swift:78:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRelatedModels.swift:79:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRelatedModels.swift:80:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRelatedModels.swift:250:15: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureRelatedModels.swift:366:15: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureRelatedModels.swift:386:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRelatedModels.swift:390:101: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureRelatedModels.swift:391:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRelatedModels.swift:393:96: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureRefPresentation.swift:142:12: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/CaptureCore/CaptureRefPresentation.swift:142:12: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/CaptureCore/CaptureRefPresentation.swift:74:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureRefPresentation.swift:75:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureRefPresentation.swift:101:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRefPresentation.swift:142:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CaptureRefPresentation.swift:143:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CaptureRefPresentation.swift:144:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CaptureRefPresentation.swift:223:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRefPresentation.swift:225:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRefPresentation.swift:233:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRefPresentation.swift:238:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRefPresentation.swift:247:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CaptureRefPresentation.swift:281:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRefPresentation.swift:321:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureRefFileUnder.swift:100:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureProjectNotePresentation.swift:187:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureProjectNotePresentation.swift:188:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureProjectNotePresentation.swift:313:1: warning: [Indentation] unindent by 4 spaces
Sources/CaptureCore/CaptureProjectNotePresentation.swift:314:1: warning: [Indentation] unindent by 4 spaces
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:600:18: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:258:26: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:302:24: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:319:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:329:1: warning: [Indentation] indent by 2 spaces
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:375:27: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:402:1: warning: [Indentation] indent by 2 spaces
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:403:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:405:1: warning: [Indentation] indent by 2 spaces
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:412:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:420:22: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:424:95: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:465:1: warning: [Indentation] indent by 2 spaces
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:471:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:520:23: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:523:23: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:533:21: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:665:23: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:702:33: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:791:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:792:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CapturePomodoroStartPresentation.swift:792:31: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroShiftPresentation.swift:76:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePomodoroResetPresentation.swift:88:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePomodoroResetPresentation.swift:90:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePomodoroLinkPresentation.swift:85:28: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroLinkPresentation.swift:97:26: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroLinkPresentation.swift:130:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroLinkPresentation.swift:158:25: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroLinkPresentation.swift:179:27: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroLineTokens.swift:189:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePomodoroClosePresentation.swift:283:37: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroClosePresentation.swift:290:23: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroClosePresentation.swift:333:31: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroClosePresentation.swift:597:31: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroClosePresentation.swift:661:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePomodoroClosePresentation.swift:888:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/CapturePomodoroClosePresentation.swift:896:22: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePomodoroBlockPresentation.swift:121:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CapturePomodoroAdjustPresentation.swift:74:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePlanBudgetPresentation.swift:51:23: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePickerPresentation.swift:188:22: warning: [Spacing] add 1 space
Sources/CaptureCore/CapturePickerPresentation.swift:190:22: warning: [Spacing] add 1 space
Sources/CaptureCore/CapturePickerPresentation.swift:192:22: warning: [Spacing] add 1 space
Sources/CaptureCore/CapturePickerPresentation.swift:194:22: warning: [Spacing] add 1 space
Sources/CaptureCore/CapturePickerPresentation.swift:196:22: warning: [Spacing] add 1 space
Sources/CaptureCore/CapturePickerPresentation.swift:198:23: warning: [Spacing] add 1 space
Sources/CaptureCore/CapturePickerPresentation.swift:200:22: warning: [Spacing] add 1 space
Sources/CaptureCore/CapturePickerPresentation.swift:202:22: warning: [Spacing] add 1 space
Sources/CaptureCore/CapturePickerPresentation.swift:204:51: warning: [Spacing] add 1 space
Sources/CaptureCore/CapturePickerPresentation.swift:206:22: warning: [Spacing] add 1 space
Sources/CaptureCore/CapturePickerPresentation.swift:208:55: warning: [Spacing] add 1 space
Sources/CaptureCore/CapturePickerPresentation.swift:553:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:555:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:557:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:559:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:561:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:563:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:565:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:567:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:570:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:572:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:574:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:576:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:757:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:759:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:761:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:763:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:765:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:767:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:769:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:771:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:774:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:776:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:778:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:780:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:945:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CapturePickerPresentation.swift:946:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CapturePickerPresentation.swift:946:35: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePickerPresentation.swift:995:24: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePickerPresentation.swift:1313:1: warning: [LineLength] line is too long
Sources/CaptureCore/CapturePickerPresentation.swift:1424:100: warning: [AddLines] add 1 line break
Sources/CaptureCore/CapturePickerHelpers.swift:71:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureOpenPlan.swift:214:24: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureOpenPlan.swift:215:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureOpenPlan.swift:216:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureOpenPlan.swift:217:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureOpenPlan.swift:218:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureOpenPlan.swift:219:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureOpenPlan.swift:222:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureOpenPlan.swift:224:20: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureOpenPlan.swift:225:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureOpenPlan.swift:226:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureOpenPlan.swift:227:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureOpenPlan.swift:228:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureOpenPlan.swift:229:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureOpenPlan.swift:243:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureNotePullPresentation.swift:44:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureNotePullPresentation.swift:60:24: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureNotePullPresentation.swift:61:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureNotePullPresentation.swift:62:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureNotePullPresentation.swift:63:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureNotePullPresentation.swift:64:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureModels.swift:36:95: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureModels.swift:122:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:342:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:360:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:392:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:578:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:879:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:1278:19: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureModels.swift:1330:19: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureModels.swift:1380:19: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureModels.swift:1519:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:2802:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:2804:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:2806:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:4195:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:4319:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:4392:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:4404:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:4855:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:4862:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:4866:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:4867:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:4989:96: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureModels.swift:5018:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:5350:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:5353:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:5382:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:5390:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:5470:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:5648:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:6626:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:7022:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:7160:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:7450:96: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureModels.swift:7678:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:7836:98: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureModels.swift:7871:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:8626:101: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureModels.swift:9438:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:9461:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:9462:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:9479:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:9487:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:9498:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:9740:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:10018:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:10099:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureModels.swift:10222:101: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureInboxRoutePresentation.swift:153:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureInboxRoutePresentation.swift:406:1: warning: [LineLength] line is too long
Sources/CaptureCore/CaptureEditWrite.swift:13:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureEditWrite.swift:14:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureEditWrite.swift:21:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureEditWrite.swift:22:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureEditWrite.swift:23:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureCloseTaskCommaProvenance.swift:88:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureCloseTaskCommaProvenance.swift:89:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureCloseTaskCommaProvenance.swift:95:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureCloseTaskCommaProvenance.swift:96:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureCloseTaskCommaProvenance.swift:97:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureCloseTaskCommaAssist.swift:66:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureCloseTaskCommaAssist.swift:67:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureCloseTaskCommaAssist.swift:68:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureCloseTaskCommaAssist.swift:69:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureCloseTaskCommaAssist.swift:78:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureCloseTaskCommaAssist.swift:79:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/CaptureAgendaPresentation.swift:525:31: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaPresentation.swift:684:26: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaPresentation.swift:685:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaPresentation.swift:686:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaPresentation.swift:687:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaPresentation.swift:688:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaPresentation.swift:689:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaPresentation.swift:690:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaPresentation.swift:691:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaPresentation.swift:693:41: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaPresentation.swift:696:39: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaPresentation.swift:799:25: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaPresentation.swift:799:43: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaPresentation.swift:799:48: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaPresentation.swift:800:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaPresentation.swift:801:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaPresentation.swift:802:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaPresentation.swift:803:26: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaPresentation.swift:1022:28: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaPresentation.swift:1047:21: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaPresentation.swift:1629:25: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaPresentation.swift:1630:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaPresentation.swift:1631:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaPresentation.swift:1644:23: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaPresentation.swift:1647:50: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaPresentation.swift:1653:46: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaPresentation.swift:2138:19: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaModels.swift:155:27: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaModels.swift:156:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:157:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:158:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:159:20: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaModels.swift:160:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:161:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:162:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:213:19: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaModels.swift:214:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:215:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:216:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:216:10: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaModels.swift:217:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:218:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:327:19: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaModels.swift:426:21: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaModels.swift:427:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:428:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:429:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:439:22: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaModels.swift:440:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:441:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:442:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:691:19: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaModels.swift:873:15: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaModels.swift:874:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:875:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:876:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:886:19: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaModels.swift:1056:17: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaModels.swift:1057:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:1058:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:1059:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:1060:15: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaModels.swift:1061:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:1062:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaModels.swift:1063:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:127:22: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:128:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:129:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:130:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:131:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:132:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:133:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:133:18: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:138:22: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:139:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:140:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:141:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:142:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:143:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:143:18: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:354:32: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:354:43: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:355:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:356:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:357:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:358:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:490:20: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:491:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:492:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:493:24: warning: [Spacing] remove 1 space
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:493:28: warning: [Spacing] remove 1 space
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:545:21: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:571:21: warning: [AddLines] add 1 line break
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:572:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:573:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:574:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:575:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:594:1: warning: [Indentation] unindent by 1 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:595:1: warning: [Indentation] unindent by 1 spaces
Sources/CaptureCore/CaptureAgendaFitPlanner.swift:596:1: warning: [Indentation] unindent by 1 spaces
Sources/CaptureCore/CanceledDraftStashStore.swift:66:15: warning: [AddLines] add 1 line break
Sources/CaptureCore/BobProcessClient.swift:116:19: warning: [AddLines] add 1 line break
Sources/CaptureCore/BobProcessClient.swift:230:1: warning: [LineLength] line is too long
Sources/CaptureCore/BobProcessClient.swift:507:1: warning: [LineLength] line is too long
Sources/CaptureCore/BobProcessClient.swift:507:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/BobProcessClient.swift:647:1: warning: [LineLength] line is too long
Sources/CaptureCore/BobProcessClient.swift:788:1: warning: [LineLength] line is too long
Sources/CaptureCore/BobProcessClient.swift:955:1: warning: [LineLength] line is too long
Sources/CaptureCore/BobProcessClient.swift:1125:1: warning: [LineLength] line is too long
Sources/CaptureCore/BobProcessClient.swift:1391:1: warning: [LineLength] line is too long
Sources/CaptureCore/BobProcessClient.swift:1494:1: warning: [LineLength] line is too long
Sources/CaptureCore/BobExecutableResolver.swift:20:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/BobErrors.swift:20:1: warning: [LineLength] line is too long
Sources/CaptureCore/BlockIDRules.swift:21:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/BlockIDRules.swift:102:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/BlockIDRules.swift:103:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/BlockIDRules.swift:104:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/BlockIDRules.swift:107:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/BlockIDRules.swift:108:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:230:1: warning: [LineLength] line is too long
Sources/CaptureCore/BlockIDPickerIndex.swift:412:1: warning: [LineLength] line is too long
Sources/CaptureCore/BlockIDPickerIndex.swift:424:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/BlockIDPickerIndex.swift:425:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:426:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:427:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:428:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:429:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:446:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/BlockIDPickerIndex.swift:447:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:448:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:449:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:450:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:451:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:461:33: warning: [AddLines] add 1 line break
Sources/CaptureCore/BlockIDPickerIndex.swift:462:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:463:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:464:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:465:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:466:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:467:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:555:32: warning: [AddLines] add 1 line break
Sources/CaptureCore/BlockIDPickerIndex.swift:556:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:557:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:558:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:559:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:560:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:620:1: warning: [LineLength] line is too long
Sources/CaptureCore/BlockIDPickerIndex.swift:639:1: warning: [LineLength] line is too long
Sources/CaptureCore/BlockIDPickerIndex.swift:642:1: warning: [LineLength] line is too long
Sources/CaptureCore/BlockIDPickerIndex.swift:729:1: warning: [LineLength] line is too long
Sources/CaptureCore/BlockIDPickerIndex.swift:776:40: warning: [AddLines] add 1 line break
Sources/CaptureCore/BlockIDPickerIndex.swift:802:1: warning: [LineLength] line is too long
Sources/CaptureCore/BlockIDPickerIndex.swift:909:1: warning: [LineLength] line is too long
Sources/CaptureCore/BlockIDPickerIndex.swift:994:25: warning: [AddLines] add 1 line break
Sources/CaptureCore/BlockIDPickerIndex.swift:1006:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/BlockIDPickerIndex.swift:1073:1: warning: [LineLength] line is too long
Sources/CaptureCore/BlockIDPickerIndex.swift:1097:24: warning: [AddLines] add 1 line break
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:19:1: warning: [LineLength] line is too long
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:51:1: warning: [LineLength] line is too long
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:124:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:125:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:126:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:127:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:128:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:129:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:130:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:131:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:132:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:135:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:136:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:137:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:138:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:139:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:140:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:143:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:144:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:145:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:146:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:147:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:148:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:151:29: warning: [AddLines] add 1 line break
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:152:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:153:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:154:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:155:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:156:1: warning: [Indentation] indent by 4 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:314:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:315:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:316:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:317:1: warning: [Indentation] unindent by 2 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:377:1: warning: [Indentation] indent by 1 spaces
Sources/CaptureCore/ActiveTaskPickerPresentation.swift:409:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCaptureInstallHelper/InstallRelauncher.swift:37:1: warning: [LineLength] line is too long
Sources/BobMacCapture/VaultTargetWatcher.swift:116:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/VaultTargetWatcher.swift:117:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/VaultTargetWatcher.swift:118:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/VaultTargetWatcher.swift:119:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/VaultTargetWatcher.swift:120:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/VaultTargetWatcher.swift:121:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/VaultTargetWatcher.swift:122:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/VaultTargetWatcher.swift:123:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/VaultTargetWatcher.swift:124:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/VaultTargetWatcher.swift:124:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/VaultTargetWatcher.swift:166:22: warning: [AddLines] add 1 line break
Sources/BobMacCapture/StatusItemController.swift:76:29: warning: [AddLines] add 1 line break
Sources/BobMacCapture/StatusItemController.swift:77:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/StatusItemController.swift:78:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/StatusItemController.swift:79:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/StatusItemController.swift:80:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/StatusItemController.swift:81:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Signposts.swift:31:1: warning: [LineLength] line is too long
Sources/BobMacCapture/SettingsView.swift:33:1: warning: [LineLength] line is too long
Sources/BobMacCapture/SettingsView.swift:250:1: warning: [LineLength] line is too long
Sources/BobMacCapture/SettingsView.swift:318:1: warning: [LineLength] line is too long
Sources/BobMacCapture/SettingsView.swift:325:1: warning: [LineLength] line is too long
Sources/BobMacCapture/SettingsView.swift:351:96: warning: [AddLines] add 1 line break
Sources/BobMacCapture/SettingsView.swift:429:38: warning: [AddLines] add 1 line break
Sources/BobMacCapture/SettingsView.swift:455:19: warning: [AddLines] add 1 line break
Sources/BobMacCapture/SettingsView.swift:459:22: warning: [AddLines] add 1 line break
Sources/BobMacCapture/SavedTemplateShelf.swift:88:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/SavedTemplateShelf.swift:89:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/SavedTemplateShelf.swift:90:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/SavedTemplateShelf.swift:91:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/RelationLabelField.swift:81:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/PomodoroThemeViews.swift:20:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/PomodoroNameField.swift:86:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/PomodoroHomeColor.swift:60:1: warning: [LineLength] line is too long
Sources/BobMacCapture/PlainTextPaste.swift:30:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/PlainTextPaste.swift:31:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/PlainTextPaste.swift:50:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/PlainTextPaste.swift:97:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/PlainTextPaste.swift:112:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/PlainTextPaste.swift:130:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/PlainTextPaste.swift:137:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/PlainTextPaste.swift:235:1: warning: [Indentation] unindent by 2 spaces
/tmp/bob-mac-capture-go12.BHqRrC/Sources/BobMacCapture/NotificationService.swift:264:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Sources/BobMacCapture/NotificationService.swift:40:1: warning: [LineLength] line is too long
Sources/BobMacCapture/NotificationService.swift:43:1: warning: [LineLength] line is too long
Sources/BobMacCapture/NotificationService.swift:46:1: warning: [LineLength] line is too long
Sources/BobMacCapture/NotificationService.swift:56:1: warning: [LineLength] line is too long
Sources/BobMacCapture/NotificationService.swift:98:28: warning: [AddLines] add 1 line break
Sources/BobMacCapture/NotificationService.swift:99:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/NotificationService.swift:100:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/NotificationService.swift:101:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/NotificationService.swift:102:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/NotificationService.swift:204:1: warning: [LineLength] line is too long
Sources/BobMacCapture/NotificationService.swift:236:1: warning: [LineLength] line is too long
Sources/BobMacCapture/NotificationService.swift:441:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/NotificationService.swift:442:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/NotificationService.swift:443:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/NotificationService.swift:443:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/NotificationService.swift:567:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/NotificationService.swift:568:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/NotificationService.swift:637:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/NotificationService.swift:708:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/NotificationService.swift:709:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/NotificationService.swift:710:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/NotificationService.swift:711:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/NotificationService.swift:712:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/NotificationService.swift:713:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/NotificationService.swift:714:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/NotificationService.swift:747:1: warning: [LineLength] line is too long
Sources/BobMacCapture/NotificationService.swift:759:1: warning: [LineLength] line is too long
Sources/BobMacCapture/NotificationService.swift:779:25: warning: [AddLines] add 1 line break
Sources/BobMacCapture/NotificationService.swift:804:30: warning: [AddLines] add 1 line break
Sources/BobMacCapture/NotificationService.swift:816:27: warning: [AddLines] add 1 line break
Sources/BobMacCapture/NotificationService.swift:819:25: warning: [AddLines] add 1 line break
Sources/BobMacCapture/NotificationService.swift:840:22: warning: [AddLines] add 1 line break
Sources/BobMacCapture/NotificationService.swift:842:23: warning: [AddLines] add 1 line break
Sources/BobMacCapture/NotificationService.swift:844:22: warning: [AddLines] add 1 line break
Sources/BobMacCapture/NotificationService.swift:846:26: warning: [AddLines] add 1 line break
Sources/BobMacCapture/NotificationService.swift:855:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/NotificationService.swift:856:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/NotificationService.swift:918:23: warning: [AddLines] add 1 line break
Sources/BobMacCapture/NotificationService.swift:944:34: warning: [AddLines] add 1 line break
Sources/BobMacCapture/NotificationService.swift:945:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/NotificationService.swift:946:1: warning: [LineLength] line is too long
Sources/BobMacCapture/NotificationService.swift:946:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/NotificationService.swift:947:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/NotificationService.swift:948:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/NotificationService.swift:951:28: warning: [AddLines] add 1 line break
Sources/BobMacCapture/NotificationService.swift:961:54: warning: [AddLines] add 1 line break
Sources/BobMacCapture/NotificationService.swift:965:34: warning: [AddLines] add 1 line break
Sources/BobMacCapture/NotificationService.swift:966:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/NotificationService.swift:967:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/NotificationService.swift:968:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/NotificationService.swift:980:30: warning: [AddLines] add 1 line break
Sources/BobMacCapture/NotificationService.swift:994:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/NotificationService.swift:995:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/NotificationService.swift:996:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/NotificationService.swift:997:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/NotificationService.swift:1039:1: warning: [LineLength] line is too long
Sources/BobMacCapture/NotificationService.swift:1116:19: warning: [AddLines] add 1 line break
Sources/BobMacCapture/NotificationService.swift:1183:98: warning: [AddLines] add 1 line break
Sources/BobMacCapture/HotKeyRegistry.swift:167:35: warning: [GroupNumericLiterals] group every 4 digits in this hexadecimal literal using a '_' separator
Sources/BobMacCapture/HighlightsTakeover.swift:85:30: warning: [AddLines] add 1 line break
Sources/BobMacCapture/HighlightsTakeover.swift:231:32: warning: [AddLines] add 1 line break
Sources/BobMacCapture/HighlightsSaveKeyMonitor.swift:51:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/HighlightsSaveKeyMonitor.swift:51:63: warning: [AddLines] add 1 line break
Sources/BobMacCapture/HighlightsSaveKeyMonitor.swift:51:82: warning: [AddLines] add 1 line break
Sources/BobMacCapture/HighlightsSaveKeyMonitor.swift:52:1: warning: [Indentation] indent by 8 spaces
Sources/BobMacCapture/HighlightsSaveKeyMonitor.swift:53:1: warning: [Indentation] indent by 8 spaces
Sources/BobMacCapture/HighlightsSaveKeyMonitor.swift:53:11: warning: [AddLines] add 1 line break
Sources/BobMacCapture/HighlightsSaveKeyMonitor.swift:174:28: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:16:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:17:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:18:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureTargetsRefreshGate.swift:19:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureSnippetResolver.swift:38:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CaptureSnippetResolver.swift:39:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePullInChoice.swift:809:22: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Sources/BobMacCapture/CapturePullInChoice.swift:147:25: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePullInChoice.swift:665:23: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePickerView.swift:1324:14: warning: [AlwaysUseLowerCamelCase] rename the function 'CapturePickerUsageDidInsert' using lowerCamelCase
Sources/BobMacCapture/CapturePickerView.swift:180:1: warning: [Indentation] unindent by 6 spaces
Sources/BobMacCapture/CapturePickerView.swift:184:1: warning: [Indentation] unindent by 6 spaces
Sources/BobMacCapture/CapturePickerView.swift:185:1: warning: [Indentation] unindent by 6 spaces
Sources/BobMacCapture/CapturePickerView.swift:259:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePickerView.swift:260:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePickerView.swift:278:22: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePickerView.swift:279:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:280:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:281:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:282:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:282:18: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePickerView.swift:283:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:284:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:285:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:303:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerView.swift:304:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:305:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:306:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:307:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerView.swift:335:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerView.swift:408:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePickerView.swift:500:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePickerView.swift:501:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePickerView.swift:537:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerView.swift:540:23: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePickerView.swift:549:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerView.swift:552:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerView.swift:597:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerView.swift:598:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:599:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:600:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:618:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerView.swift:619:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:620:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:621:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:715:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerView.swift:716:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:717:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:718:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:797:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerView.swift:840:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerView.swift:905:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerView.swift:906:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerView.swift:909:28: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePickerView.swift:910:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:911:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:912:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:913:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:914:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:915:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:916:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:917:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:918:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:919:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:920:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:921:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:922:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:923:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:924:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:924:22: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePickerView.swift:925:1: warning: [Indentation] indent by 8 spaces
Sources/BobMacCapture/CapturePickerView.swift:926:1: warning: [Indentation] indent by 8 spaces
Sources/BobMacCapture/CapturePickerView.swift:927:1: warning: [Indentation] indent by 8 spaces
Sources/BobMacCapture/CapturePickerView.swift:928:1: warning: [Indentation] indent by 8 spaces
Sources/BobMacCapture/CapturePickerView.swift:928:18: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePickerView.swift:929:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:930:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:931:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:932:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:933:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:934:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:936:24: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePickerView.swift:937:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:938:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:938:22: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePickerView.swift:939:1: warning: [Indentation] indent by 8 spaces
Sources/BobMacCapture/CapturePickerView.swift:940:1: warning: [Indentation] indent by 8 spaces
Sources/BobMacCapture/CapturePickerView.swift:941:1: warning: [Indentation] indent by 8 spaces
Sources/BobMacCapture/CapturePickerView.swift:942:1: warning: [Indentation] indent by 8 spaces
Sources/BobMacCapture/CapturePickerView.swift:942:18: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePickerView.swift:943:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:944:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:945:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:946:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:947:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:948:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:949:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:950:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:950:22: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePickerView.swift:951:1: warning: [Indentation] indent by 8 spaces
Sources/BobMacCapture/CapturePickerView.swift:952:1: warning: [Indentation] indent by 8 spaces
Sources/BobMacCapture/CapturePickerView.swift:953:1: warning: [Indentation] indent by 8 spaces
Sources/BobMacCapture/CapturePickerView.swift:954:1: warning: [Indentation] indent by 8 spaces
Sources/BobMacCapture/CapturePickerView.swift:954:18: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePickerView.swift:955:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:956:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:957:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:958:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:959:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:960:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:1044:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerView.swift:1053:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerView.swift:1113:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerView.swift:1114:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePickerView.swift:1135:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePickerView.swift:1140:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePickerView.swift:1145:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePickerView.swift:1149:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerView.swift:1168:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerView.swift:1172:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePickerFilterField.swift:95:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelView.swift:68:37: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:77:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:81:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:82:45: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:113:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:361:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:374:31: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:375:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:376:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:377:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:407:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:697:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:698:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:699:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:700:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:701:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:702:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:703:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:1005:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelView.swift:1006:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelView.swift:1007:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelView.swift:1046:25: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:1047:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:1048:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:1049:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:1073:25: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:1074:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:1084:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:1236:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:1266:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:1268:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:1419:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:1442:29: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:1560:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelView.swift:1702:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:1836:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:1943:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:1970:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:1982:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:1984:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:1986:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:1988:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:1990:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:1992:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:1993:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:1997:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:1999:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:2005:100: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:2005:108: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:2009:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:2011:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:2013:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:2015:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:2092:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:2145:63: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:2351:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2380:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelView.swift:2395:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:2415:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:2415:1: warning: [Indentation] unindent by 6 spaces
Sources/BobMacCapture/CapturePanelView.swift:2428:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2429:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2430:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2431:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2432:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2433:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2434:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2435:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2436:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2437:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2438:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2439:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2440:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2441:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2442:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2443:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2444:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2445:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2446:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2447:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2448:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2449:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2450:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2451:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2452:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2453:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2454:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2455:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2456:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2457:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2458:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2459:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2460:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2461:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2462:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2463:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:2463:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2464:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2465:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2466:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2467:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2468:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2469:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2470:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2471:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2472:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2473:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2474:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2475:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2476:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2477:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2478:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2479:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2480:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2481:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2482:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2483:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2484:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2485:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2486:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2487:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2488:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2489:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2490:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2491:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2492:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2493:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2494:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2495:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2496:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2497:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2498:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2499:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2500:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2501:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2502:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2503:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2504:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2505:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2506:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2507:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2508:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2509:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2509:60: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:2509:101: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:2510:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2511:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2512:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2513:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2514:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2515:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2516:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2517:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:2517:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2518:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2519:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2520:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2521:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2522:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2523:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2524:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2525:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2526:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2527:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2528:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2529:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2530:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2531:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:2532:18: warning: [Spacing] add 1 space
Sources/BobMacCapture/CapturePanelView.swift:2748:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:2776:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelView.swift:2804:92: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:2893:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:3166:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:3377:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:3727:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:3752:1: warning: [Indentation] unindent by 6 spaces
Sources/BobMacCapture/CapturePanelView.swift:3881:30: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:3882:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:3883:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:3903:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelView.swift:3904:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelView.swift:3905:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelView.swift:3906:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelView.swift:3907:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelView.swift:3908:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelView.swift:3912:28: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:3940:1: warning: [Indentation] unindent by 6 spaces
Sources/BobMacCapture/CapturePanelView.swift:4197:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:4748:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:4850:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:4893:22: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:5259:22: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:5431:35: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:5443:35: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:5669:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelView.swift:5734:33: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:5735:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:5736:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:5737:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:5738:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:5739:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:5740:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:5749:33: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:5750:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:5751:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:5752:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:5753:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:5754:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:5755:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:5900:87: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:5903:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:5904:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:5905:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:5952:92: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:5962:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:6013:33: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:6014:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6015:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6016:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6017:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6018:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6235:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelView.swift:6309:29: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:6310:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6311:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6312:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6313:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6314:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6315:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6328:28: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:6329:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6330:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6331:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6332:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6333:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6335:24: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:6336:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6337:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6400:29: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:6401:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6402:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6403:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6404:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6405:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6406:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6467:29: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:6468:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6469:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6470:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6471:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6472:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6473:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6517:27: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:6519:28: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:6521:27: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:6523:27: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:6531:27: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:6533:33: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:6535:26: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:6536:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6536:61: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:6538:32: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:6539:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6539:40: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:6642:29: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelView.swift:6643:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6644:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6645:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6646:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6647:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelView.swift:6648:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:3:1: warning: [OrderedImports] sort import statements lexicographically
/tmp/bob-mac-capture-go12.BHqRrC/Sources/BobMacCapture/CapturePanelModel.swift:9702:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Sources/BobMacCapture/CapturePanelModel.swift:500:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:506:1: warning: [Indentation] replace leading whitespace with 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:507:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:508:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:509:1: warning: [Indentation] replace leading whitespace with 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:537:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:538:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:546:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:596:32: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:596:34: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:597:1: warning: [Indentation] indent by 8 spaces
Sources/BobMacCapture/CapturePanelModel.swift:598:1: warning: [Indentation] indent by 8 spaces
Sources/BobMacCapture/CapturePanelModel.swift:599:1: warning: [Indentation] indent by 8 spaces
Sources/BobMacCapture/CapturePanelModel.swift:600:1: warning: [Indentation] indent by 8 spaces
Sources/BobMacCapture/CapturePanelModel.swift:600:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:605:20: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:606:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:607:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:608:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:609:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:610:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:614:24: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:615:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:616:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:617:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:618:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:619:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:620:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:621:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:695:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:711:1: warning: [Indentation] replace leading whitespace with 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:712:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:713:1: warning: [Indentation] replace leading whitespace with 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:734:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:735:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:736:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:737:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:987:25: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:1284:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:1325:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:1429:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:1598:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:1599:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:1694:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:1695:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:1696:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:1697:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:1698:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:1699:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:1700:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:1727:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:1728:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:1737:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:1738:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:1739:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:1843:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2197:97: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:2220:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2221:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2337:1: warning: [Indentation] unindent by 6 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2338:1: warning: [Indentation] unindent by 6 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2339:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:2339:1: warning: [Indentation] unindent by 6 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2375:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2376:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2469:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2487:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2510:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2570:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2571:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2572:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2573:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2574:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2575:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2632:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2633:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2643:1: warning: [Indentation] unindent by 6 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2649:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2650:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2667:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2668:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2669:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2727:28: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:2727:41: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:2728:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2729:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2730:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2731:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2732:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2733:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2734:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2735:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2736:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2737:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2738:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2739:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2740:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2741:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2742:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2743:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2767:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:2794:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2795:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2796:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2820:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:2825:19: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:2826:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2827:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2828:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2829:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2830:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2831:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2832:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2833:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2834:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2835:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2835:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:2836:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2837:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2838:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2839:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2840:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2841:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2842:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:2843:23: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:2867:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:2935:38: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:2936:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:2958:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:3018:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:3032:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:3033:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:3042:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:3092:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:3093:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:3163:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:3185:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:3243:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:3244:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:3245:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:3615:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:4185:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:4613:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:4614:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:4615:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:4616:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:4658:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:4659:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:4660:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:4781:15: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:4791:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:4849:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:4881:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:4882:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:4883:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:4884:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5019:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5064:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5092:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5093:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5094:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5095:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5164:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5182:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5183:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5184:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5185:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5262:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5269:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:5269:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5286:20: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:5286:37: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:5287:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5288:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5289:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5290:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5291:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5295:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5296:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5297:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5298:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5301:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:5368:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:5390:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5416:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5432:20: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:5432:37: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:5433:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5434:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5435:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5436:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5440:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5441:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5442:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:5442:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5443:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5499:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5500:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5527:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:5546:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:5561:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:5569:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:5572:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5601:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5628:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5629:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5630:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5631:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5692:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5716:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:5751:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5752:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5753:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5754:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5807:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5822:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:5826:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5827:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5828:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5829:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5897:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5904:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5905:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5906:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5907:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5936:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5937:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5938:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5939:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:5997:100: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:5997:110: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:6000:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6010:100: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:6010:110: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:6013:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6090:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6125:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6126:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6249:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6250:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6251:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6259:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6280:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6294:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6319:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6320:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6330:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6340:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6341:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6342:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6343:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6364:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6365:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6366:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6367:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6368:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6419:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6420:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6492:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6493:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6534:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6543:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6554:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6555:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6571:28: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:6603:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6604:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:6604:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6615:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:6628:100: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:6636:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:6687:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:6709:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6766:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:6801:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:6803:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:6821:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6822:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6823:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6824:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6831:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6832:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6833:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6834:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6835:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6836:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6837:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6838:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6839:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:6853:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:6855:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:6901:98: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:6901:123: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:7015:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7016:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7017:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7023:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7024:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7025:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7026:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7027:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7028:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7029:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7055:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7060:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:7060:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7105:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7110:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:7110:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7163:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7164:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7165:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7166:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7167:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7168:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7169:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7175:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7218:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:7218:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7247:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7248:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7264:18: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:7265:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7266:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7267:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7268:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7268:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:7283:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7284:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7285:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7344:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7362:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7380:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7401:27: warning: [Spacing] add 1 space
Sources/BobMacCapture/CapturePanelModel.swift:7403:27: warning: [Spacing] add 1 space
Sources/BobMacCapture/CapturePanelModel.swift:7405:27: warning: [Spacing] add 1 space
Sources/BobMacCapture/CapturePanelModel.swift:7407:27: warning: [Spacing] add 1 space
Sources/BobMacCapture/CapturePanelModel.swift:7409:28: warning: [Spacing] add 1 space
Sources/BobMacCapture/CapturePanelModel.swift:7411:27: warning: [Spacing] add 1 space
Sources/BobMacCapture/CapturePanelModel.swift:7414:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7415:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7416:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7432:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7433:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7434:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7435:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7471:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7472:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7491:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:7522:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:7527:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7528:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7529:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7542:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:7614:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:7630:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:7638:98: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:7646:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:7656:30: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:7657:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7658:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7659:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7660:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7660:26: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:7673:30: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:7674:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7675:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7676:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7677:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:7677:26: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:7797:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:7809:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:7943:100: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:7952:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:8045:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8046:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:8046:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8060:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:8123:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:8123:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8166:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8167:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8168:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8169:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8187:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8212:18: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:8213:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8214:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8215:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8216:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8216:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:8230:18: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:8231:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8232:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8233:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8234:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8234:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:8273:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:8364:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:8386:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:8403:29: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:8508:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8509:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8533:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8534:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:8582:95: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:8583:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:8589:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:9002:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9010:101: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:9010:109: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:9019:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9020:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9053:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9066:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9067:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9068:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9069:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9070:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9071:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9083:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9084:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9085:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9106:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9107:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9129:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9143:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9144:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9145:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9173:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:9339:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9359:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9366:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9367:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9404:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9405:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9406:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9407:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9417:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9418:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9419:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9430:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9431:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9477:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9478:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9517:1: warning: [Indentation] unindent by 6 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9518:1: warning: [Indentation] unindent by 6 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9519:1: warning: [Indentation] unindent by 6 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9593:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9594:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9632:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9633:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9634:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9635:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9636:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9637:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9668:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9669:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9670:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9671:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9672:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9673:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9680:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9691:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:9716:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9717:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9718:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9719:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9720:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9721:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9761:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9762:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9763:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9779:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9780:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9807:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9808:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9809:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9810:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9811:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9855:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9856:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9864:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9886:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9887:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9888:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9971:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:9972:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10000:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:10047:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10048:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10129:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:10129:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10144:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:10153:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10154:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10155:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10156:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10156:11: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:10170:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10171:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10172:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10184:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:10209:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10210:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10211:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10239:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10276:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10277:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10280:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:10307:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10308:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10329:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:10337:94: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:10337:101: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:10386:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:10410:22: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:10411:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10412:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10413:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10413:18: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:10414:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:10422:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:10502:100: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:10503:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:10511:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:10550:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10554:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10573:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10574:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10590:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:10603:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:10603:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10604:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10605:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10611:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:10631:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10632:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10633:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10639:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:10653:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10654:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10655:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10656:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10672:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10673:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10681:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10682:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10699:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:10719:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10720:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10721:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10751:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10752:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10753:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10754:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10771:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10808:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10809:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10827:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10828:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10828:94: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:10836:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10837:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10838:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10843:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10844:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10844:100: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:10857:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:10858:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10859:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10860:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10861:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10862:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10863:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10871:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10872:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10873:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10890:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:10905:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:10907:25: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:10933:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11064:95: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11065:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:11081:94: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11081:102: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11089:99: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11089:107: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11109:99: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11109:114: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11121:1: warning: [Indentation] unindent by 6 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11127:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:11140:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:11215:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11216:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11217:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11218:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11251:38: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11273:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11274:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11289:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11290:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11291:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11305:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11306:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11307:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11308:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11309:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11356:24: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11357:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11358:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11358:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11359:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11360:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11361:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11362:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11363:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11364:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11411:24: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11412:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11413:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11413:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11414:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11415:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11416:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11417:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11418:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11419:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11453:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11454:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11455:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:11455:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11501:24: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11502:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11503:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11503:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11504:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11505:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11506:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11507:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11508:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11509:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11553:24: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11554:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:11554:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11555:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11555:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11556:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11557:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11558:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11559:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11560:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11561:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11604:24: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11605:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:11605:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11606:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11606:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11607:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11608:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11609:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11610:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11611:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11612:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11648:24: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11649:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:11649:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11650:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11650:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11651:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11652:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11653:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11654:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11655:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11656:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11698:24: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11699:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:11699:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11700:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11700:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11701:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11702:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11703:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11704:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11705:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11706:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11748:24: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11749:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:11749:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11750:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11750:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:11751:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11752:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11753:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11754:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11755:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11756:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11841:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11917:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11925:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:11927:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:11939:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:11968:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:11985:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12013:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12015:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12025:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12026:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12036:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12052:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12061:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12063:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12074:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12090:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12102:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12108:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12110:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12121:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12137:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12167:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12173:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12175:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12186:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12202:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12221:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12223:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12234:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12250:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12257:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12259:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12271:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12330:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12331:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12332:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12333:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12334:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12335:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12336:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12337:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12338:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12339:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12360:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12388:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12391:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12402:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12414:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12443:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12446:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12457:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12469:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12496:96: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:12508:100: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:12510:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12521:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12537:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12546:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12637:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12663:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12664:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12665:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12666:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12668:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12686:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12694:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12695:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12696:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12697:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12698:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12699:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12701:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12709:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12716:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12717:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12718:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12719:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12720:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12721:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12745:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:12809:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12810:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:12811:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13025:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13044:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13045:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13046:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13069:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13070:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13170:27: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:13175:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13176:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13212:35: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:13267:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13268:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13269:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13270:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13271:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13272:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13402:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13420:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13457:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13461:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13527:22: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:13528:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:13528:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13529:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13530:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13531:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13532:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13533:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13533:32: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:13538:22: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:13539:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13540:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13541:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13542:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13543:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13544:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13544:26: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:13555:26: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:13556:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13557:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13558:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13559:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13560:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13561:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13561:30: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:13620:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:13621:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13623:91: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:13640:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:13660:26: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:13661:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13662:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13663:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13664:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13665:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13666:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13666:30: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:13685:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13686:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13687:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13688:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13689:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13690:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13691:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13692:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13720:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13721:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13722:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13723:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13724:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13725:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13726:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13802:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13803:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13804:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13805:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13806:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13807:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13808:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13809:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13835:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13836:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13837:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13856:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13861:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13882:22: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:13883:1: warning: [Indentation] indent by 6 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13884:1: warning: [Indentation] indent by 6 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13885:1: warning: [Indentation] indent by 6 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13886:1: warning: [Indentation] indent by 6 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13887:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13887:18: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:13893:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13894:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13895:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13896:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13897:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13903:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13908:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13924:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13929:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13971:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:13972:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13973:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13974:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13975:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13976:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:13976:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:14010:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:14019:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:14023:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14032:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14033:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14034:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14035:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14036:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14073:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14074:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14075:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14076:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14117:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14229:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14236:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14289:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14290:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14315:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14346:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14347:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14368:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14369:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14376:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:14377:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14378:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14379:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14380:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14381:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14381:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:14386:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:14387:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14388:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:14388:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14389:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:14389:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14390:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14424:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:14478:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14498:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:14499:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14500:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14501:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14502:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14503:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14503:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:14599:36: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:14600:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14601:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14603:37: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:14637:100: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:14697:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14726:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14727:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14728:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14729:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14730:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14731:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14732:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14733:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14734:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14735:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14736:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14762:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14777:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:14779:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:14779:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14780:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14781:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14782:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14804:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:14898:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:14996:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14997:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14998:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:14999:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15000:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15001:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15002:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15003:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15004:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15005:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15006:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15007:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15013:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15014:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15015:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15029:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15030:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15031:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15032:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15033:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15076:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:15078:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15079:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15080:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15081:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15124:101: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:15131:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:15155:25: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:15162:28: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:15165:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:15175:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:15177:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:15190:21: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:15194:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:15206:28: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelModel.swift:15209:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:15216:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelModel.swift:15305:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15306:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelModel.swift:15307:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:94:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:95:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:110:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:111:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:130:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:151:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:152:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:153:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:154:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:155:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:199:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:200:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:242:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:243:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:400:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:425:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelController.swift:521:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelController.swift:546:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelController.swift:698:27: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelController.swift:790:23: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelController.swift:827:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelController.swift:868:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:869:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:870:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:892:18: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelController.swift:893:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:894:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:895:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:895:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelController.swift:903:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelController.swift:904:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:905:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:906:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:972:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:975:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:996:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:999:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1022:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1023:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1027:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1056:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1057:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1058:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1088:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1089:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1118:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:1119:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:1120:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:1137:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1138:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1139:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1140:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1160:100: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelController.swift:1165:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:1166:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:1167:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:1189:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1198:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelController.swift:1199:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:1200:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:1201:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:1201:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelController.swift:1205:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelController.swift:1206:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:1207:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:1208:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:1208:17: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelController.swift:1240:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1244:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1326:98: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelController.swift:1326:106: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelController.swift:1372:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1373:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1457:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1458:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1541:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1542:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1610:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1614:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:1649:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelController.swift:1650:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:1651:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:1652:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:1653:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:1654:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:1654:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelController.swift:1675:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:2062:95: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelController.swift:2064:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:2081:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelController.swift:2082:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2083:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2084:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2085:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2086:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2087:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2088:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2089:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CapturePanelController.swift:2089:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2090:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2091:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2092:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2093:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2094:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2095:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2096:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2097:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2098:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2099:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2100:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2101:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2102:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2103:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2104:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2105:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2106:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2107:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2108:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2109:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2110:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2111:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2112:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2113:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2114:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2115:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2116:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2117:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2118:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2119:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2120:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2121:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2122:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2123:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2124:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2125:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2126:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2127:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2128:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2128:93: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelController.swift:2129:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2130:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2131:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2131:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CapturePanelController.swift:2163:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:2167:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:2168:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:2177:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:2181:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:2182:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CapturePanelController.swift:2212:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2213:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2221:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2222:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2230:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2231:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2291:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2296:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2297:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2310:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2311:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2312:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CapturePanelController.swift:2313:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2314:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2321:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2322:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2323:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2324:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2325:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2326:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2327:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2334:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2335:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2336:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2337:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2338:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2339:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2340:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CapturePanelController.swift:2355:1: warning: [Indentation] indent by 1 spaces
/tmp/bob-mac-capture-go12.BHqRrC/Sources/BobMacCapture/CaptureKeyCommandRouter.swift:516:29: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:286:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:287:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:416:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:424:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:425:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:426:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:427:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:428:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:429:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:575:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:576:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:577:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:614:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:615:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:641:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:757:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:816:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:817:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:818:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:819:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:820:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:850:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:851:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:852:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:860:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:861:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:862:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:863:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:864:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:922:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:923:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:924:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:925:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:939:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:941:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:947:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:949:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:971:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:972:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:973:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:974:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:988:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:998:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:1000:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:1016:101: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CaptureKeyCommandRouter.swift:1022:100: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CaptureInboxRouteChoiceView.swift:38:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CaptureInboxRouteChoiceView.swift:46:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/CaptureEditorTextConfiguration.swift:46:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureEditorTextConfiguration.swift:47:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/CaptureEditorPalette.swift:19:20: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CaptureAgendaView.swift:204:1: warning: [Indentation] unindent by 1 spaces
Sources/BobMacCapture/CaptureAgendaView.swift:207:1: warning: [Indentation] unindent by 1 spaces
Sources/BobMacCapture/CaptureAgendaView.swift:208:1: warning: [Indentation] unindent by 1 spaces
Sources/BobMacCapture/CaptureAgendaView.swift:209:1: warning: [Indentation] unindent by 1 spaces
Sources/BobMacCapture/CaptureAgendaView.swift:514:1: warning: [Indentation] unindent by 1 spaces
Sources/BobMacCapture/CaptureAgendaView.swift:515:1: warning: [Indentation] unindent by 1 spaces
Sources/BobMacCapture/CaptureAgendaView.swift:516:1: warning: [Indentation] unindent by 1 spaces
Sources/BobMacCapture/CaptureAgendaView.swift:517:1: warning: [Indentation] unindent by 1 spaces
Sources/BobMacCapture/CaptureAgendaView.swift:518:1: warning: [Indentation] unindent by 1 spaces
Sources/BobMacCapture/CaptureAgendaView.swift:546:1: warning: [Indentation] unindent by 1 spaces
Sources/BobMacCapture/CaptureAgendaView.swift:547:1: warning: [Indentation] unindent by 1 spaces
Sources/BobMacCapture/CaptureAgendaView.swift:548:1: warning: [Indentation] unindent by 1 spaces
Sources/BobMacCapture/CaptureAgendaView.swift:549:1: warning: [Indentation] unindent by 1 spaces
Sources/BobMacCapture/CaptureAgendaView.swift:686:22: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CaptureAgendaView.swift:990:21: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CaptureAgendaView.swift:1157:96: warning: [RemoveLine] remove line break
Sources/BobMacCapture/CaptureAgendaStore.swift:162:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CaptureAgendaStore.swift:163:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CaptureAgendaStore.swift:164:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CaptureAgendaStore.swift:165:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/CaptureAgendaStore.swift:165:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CaptureAgendaRowMeasurer.swift:171:1: warning: [LineLength] line is too long
Sources/BobMacCapture/CaptureAgendaRowMeasurer.swift:185:23: warning: [AddLines] add 1 line break
Sources/BobMacCapture/CanceledDraftStash.swift:183:1: warning: [LineLength] line is too long
Sources/BobMacCapture/BundleSigningInspector.swift:12:1: warning: [LineLength] line is too long
Sources/BobMacCapture/BundleSigningInspector.swift:14:1: warning: [LineLength] line is too long
Sources/BobMacCapture/BundleSigningInspector.swift:38:1: warning: [LineLength] line is too long
Sources/BobMacCapture/BlockIDField.swift:86:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/BlockDiffCard.swift:64:27: warning: [AddLines] add 1 line break
Sources/BobMacCapture/BlockDiffCard.swift:65:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/BlockDiffCard.swift:66:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/BlockDiffCard.swift:67:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/BlockDiffCard.swift:68:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/BlockDiffCard.swift:69:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/BlockDiffCard.swift:70:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/BlockDiffCard.swift:71:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/BlockDiffCard.swift:72:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/BlockDiffCard.swift:73:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/AppSettings.swift:138:30: warning: [AddLines] add 1 line break
Sources/BobMacCapture/AppSettings.swift:145:28: warning: [AddLines] add 1 line break
Sources/BobMacCapture/AppSettings.swift:192:24: warning: [AddLines] add 1 line break
Sources/BobMacCapture/AppSettings.swift:195:30: warning: [AddLines] add 1 line break
Sources/BobMacCapture/AppDelegate.swift:417:1: warning: [LineLength] line is too long
Sources/BobMacCapture/AccessibilityTrust.swift:15:1: warning: [LineLength] line is too long
Sources/BobMacCapture/AccessibilityTrust.swift:71:1: warning: [LineLength] line is too long
Sources/BobMacCapture/Refs/RefsVisualTokens.swift:154:24: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsTodayLinkCardView.swift:173:91: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsTodayLinkCardView.swift:312:100: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsTodayLinkCardView.swift:414:1: warning: [LineLength] line is too long
Sources/BobMacCapture/Refs/RefsTodayLinkCardView.swift:415:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/Refs/RefsTodayLinkCardView.swift:416:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/Refs/RefsScanReceiptObserver.swift:5:1: warning: [OrderedImports] sort import statements lexicographically
Sources/BobMacCapture/Refs/RefsScanReceiptObserver.swift:6:1: warning: [OrderedImports] remove this duplicate import
Sources/BobMacCapture/Refs/RefsRenameCardView.swift:179:1: warning: [NoAccessLevelOnExtensionDeclaration] remove this 'private' access modifier and declare each member inside this extension as 'fileprivate'
Sources/BobMacCapture/Refs/RefsRenameCardView.swift:180:5: note: add 'fileprivate' access modifier to this declaration
Sources/BobMacCapture/Refs/RefsQuoteText.swift:26:19: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsQuoteText.swift:31:19: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsPanelView.swift:64:32: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsPanelView.swift:65:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsPanelView.swift:66:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsPanelView.swift:238:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanelView.swift:254:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/Refs/RefsPanelView.swift:255:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsPanelView.swift:256:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsPanelView.swift:257:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsPanelView.swift:258:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/Refs/RefsPanelView.swift:384:34: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsPanelModel.swift:518:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsPanelModel.swift:519:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsPanelModel.swift:3122:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsPanelModel.swift:3123:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:866:12: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/BobMacCapture/Refs/RefsPanel.swift:866:12: warning: [NoParensAroundConditions] remove the parentheses around this expression
Sources/BobMacCapture/Refs/RefsPanel.swift:1067:1: warning: [NoAccessLevelOnExtensionDeclaration] remove this 'private' access modifier and declare each member inside this extension as 'fileprivate'
Sources/BobMacCapture/Refs/RefsPanel.swift:1070:5: note: add 'fileprivate' access modifier to this declaration
Sources/BobMacCapture/Refs/RefsPanel.swift:252:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:253:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:440:1: warning: [LineLength] line is too long
Sources/BobMacCapture/Refs/RefsPanel.swift:466:18: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsPanel.swift:467:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:468:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:469:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:470:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:470:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsPanel.swift:477:18: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsPanel.swift:478:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:479:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:480:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:481:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:481:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsPanel.swift:562:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:571:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:580:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:591:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:598:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsPanel.swift:599:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:615:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:616:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:617:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:618:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:635:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:636:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:637:1: warning: [Indentation] indent by 3 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:660:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:677:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:692:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:732:1: warning: [LineLength] line is too long
Sources/BobMacCapture/Refs/RefsPanel.swift:737:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:749:100: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsPanel.swift:754:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:789:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:866:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:867:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:868:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:869:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:870:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:871:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:872:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:899:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:908:27: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsPanel.swift:949:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:950:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:951:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:952:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:953:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:958:48: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsPanel.swift:1014:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:1015:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:1016:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:1017:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:1018:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:1021:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/Refs/RefsPanel.swift:1029:48: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsInspectorView.swift:162:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsInspectorView.swift:163:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsInspectorView.swift:164:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsInspectorView.swift:165:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsInspectorView.swift:165:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsInspectorView.swift:416:1: warning: [LineLength] line is too long
Sources/BobMacCapture/Refs/RefsInspectorView.swift:1099:33: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsInspectorView.swift:1219:20: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsInspectorView.swift:1232:1: warning: [LineLength] line is too long
Sources/BobMacCapture/Refs/RefsInspectorView.swift:1233:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/Refs/RefsInspectorScroll.swift:108:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsInspectorScroll.swift:109:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsInspectorScroll.swift:110:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsInspectorScroll.swift:195:1: warning: [Indentation] indent by 2 spaces
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:60:1: warning: [NoAccessLevelOnExtensionDeclaration] move this 'public' access modifier to precede each member inside this extension
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:61:5: note: add 'public' access modifier to this declaration
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:628:30: warning: [ReplaceForEachWithForLoop] replace use of '.forEach { ... }' with for-in loop
/tmp/bob-mac-capture-go12.BHqRrC/Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:341:92: warning: [TrailingComma] add trailing comma to the last element in multiline collection literal
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:199:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:207:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:213:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:278:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:279:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:291:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:292:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:325:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:350:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:353:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:354:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:379:1: warning: [LineLength] line is too long
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:411:22: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:412:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:413:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:433:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsInspectorLoader.swift:896:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsFooter.swift:107:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsFooter.swift:108:1: warning: [Indentation] unindent by 2 spaces
Sources/BobMacCapture/Refs/RefsCopyHUD.swift:88:21: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsCopyHUD.swift:257:25: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/RefsCopyCardView.swift:772:1: warning: [Indentation] unindent by 4 spaces
Sources/BobMacCapture/Refs/RefsCodePreviewWell.swift:115:38: warning: [AddLines] add 1 line break
/tmp/bob-mac-capture-go12.BHqRrC/Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:517:26: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:29:1: warning: [LineLength] line is too long
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:70:1: warning: [LineLength] line is too long
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:132:18: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:133:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:134:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:135:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:135:15: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:136:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:179:1: warning: [LineLength] line is too long
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:230:1: warning: [LineLength] line is too long
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:340:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:341:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:342:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:343:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:344:1: warning: [Indentation] indent by 1 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:443:15: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:454:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:455:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:456:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:457:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:458:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:468:25: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:469:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:470:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:471:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:472:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:473:45: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:474:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:475:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:476:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:477:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:478:30: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:479:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:480:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:481:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:482:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:486:44: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:487:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:488:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:489:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:490:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:494:31: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:511:32: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:512:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:513:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:514:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:515:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:516:35: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:517:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:518:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:519:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:520:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:521:35: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:573:23: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:574:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:575:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:576:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:577:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:628:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:629:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:630:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:631:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:632:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:633:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:634:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:634:10: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:657:14: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:658:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:659:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:660:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:661:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:668:23: warning: [AddLines] add 1 line break
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:669:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:670:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:671:1: warning: [Indentation] indent by 4 spaces
Sources/BobMacCapture/Refs/AXHighlightsTabsReader.swift:672:1: warning: [Indentation] indent by 4 spaces
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsTodayTests.swift:112:76: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsTodayTests.swift:131:76: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/RefsCoreTests/RefsTodayTests.swift:39:37: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayTests.swift:39:54: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayTests.swift:40:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayTests.swift:41:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayTests.swift:42:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayTests.swift:52:37: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayTests.swift:52:54: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayTests.swift:53:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayTests.swift:54:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayTests.swift:55:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayTests.swift:102:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayTests.swift:103:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayTests.swift:104:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayTests.swift:105:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayTests.swift:107:37: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayTests.swift:107:54: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayTests.swift:108:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayTests.swift:109:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayTests.swift:117:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayTests.swift:118:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayTests.swift:119:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayTests.swift:120:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayTests.swift:121:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayTests.swift:123:37: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayTests.swift:123:54: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayTests.swift:124:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayTests.swift:125:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayTests.swift:144:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayTests.swift:145:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayTests.swift:146:1: warning: [Indentation] indent by 4 spaces
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsTodayLinkThemeTests.swift:32:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsTodayLinkThemeTests.swift:56:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsTodayLinkTests.swift:411:45: warning: [TrailingComma] add trailing comma to the last element in multiline collection literal
Tests/RefsCoreTests/RefsTodayLinkTests.swift:79:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsTodayLinkTests.swift:208:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsTodayLinkTests.swift:234:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsTodayLinkTests.swift:256:96: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayLinkTests.swift:258:95: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayLinkTests.swift:266:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsTodayLinkTests.swift:267:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsTodayLinkTests.swift:274:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsTodayLinkTests.swift:280:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsTodayLinkTests.swift:324:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsTodayLinkTests.swift:356:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsTodayLinkTests.swift:367:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsTodayLinkTests.swift:368:1: warning: [Indentation] unindent by 4 spaces
Tests/RefsCoreTests/RefsTodayLinkTests.swift:374:92: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayLinkTests.swift:379:101: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayLinkTests.swift:395:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsTodayLinkTests.swift:396:1: warning: [Indentation] indent by 2 spaces
Tests/RefsCoreTests/RefsTodayLinkTests.swift:396:43: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayLinkTests.swift:412:91: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayLinkTests.swift:413:1: warning: [Indentation] unindent by 4 spaces
Tests/RefsCoreTests/RefsTodayLinkTests.swift:429:97: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayLinkTests.swift:430:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayLinkTests.swift:435:97: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayLinkTests.swift:436:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayLinkTests.swift:442:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsTodayLinkTests.swift:470:94: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayLinkTests.swift:529:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:118:25: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:120:1: warning: [Indentation] unindent by 2 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:121:1: warning: [Indentation] unindent by 2 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:122:1: warning: [Indentation] unindent by 2 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:124:1: warning: [Indentation] unindent by 2 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:125:1: warning: [Indentation] unindent by 2 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:126:1: warning: [Indentation] unindent by 2 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:127:1: warning: [Indentation] unindent by 2 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:128:1: warning: [Indentation] unindent by 2 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:129:19: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:131:1: warning: [Indentation] unindent by 2 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:132:1: warning: [Indentation] unindent by 2 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:133:1: warning: [Indentation] unindent by 2 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:135:1: warning: [Indentation] unindent by 2 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:136:1: warning: [Indentation] unindent by 2 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:137:1: warning: [Indentation] unindent by 2 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:138:1: warning: [Indentation] unindent by 2 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:139:1: warning: [Indentation] unindent by 2 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:140:1: warning: [Indentation] unindent by 2 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:142:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:143:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTodayLinkSuggestionTests.swift:144:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTabCloseTests.swift:446:15: warning: [ReplaceForEachWithForLoop] replace use of '.forEach { ... }' with for-in loop
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsTabCloseTests.swift:87:75: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/RefsCoreTests/RefsTabCloseTests.swift:31:23: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTabCloseTests.swift:32:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTabCloseTests.swift:33:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTabCloseTests.swift:34:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTabCloseTests.swift:35:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTabCloseTests.swift:36:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTabCloseTests.swift:36:14: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTabCloseTests.swift:77:27: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTabCloseTests.swift:77:40: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTabCloseTests.swift:78:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTabCloseTests.swift:79:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTabCloseTests.swift:80:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTabCloseTests.swift:81:27: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTabCloseTests.swift:81:41: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTabCloseTests.swift:82:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTabCloseTests.swift:83:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTabCloseTests.swift:129:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTabCloseTests.swift:129:44: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTabCloseTests.swift:130:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTabCloseTests.swift:131:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTabCloseTests.swift:179:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsTabCloseTests.swift:251:25: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsTabCloseTests.swift:252:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTabCloseTests.swift:253:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTabCloseTests.swift:254:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTabCloseTests.swift:255:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsTabCloseTests.swift:256:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsSectionsTests.swift:16:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsSectionsTests.swift:16:47: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsSectionsTests.swift:17:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsSectionsTests.swift:18:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsSectionsTests.swift:30:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsSectionsTests.swift:30:55: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsSectionsTests.swift:31:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsSectionsTests.swift:32:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsSectionsTests.swift:605:26: warning: [AddLines] add 1 line break
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsScanTests.swift:294:92: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsScanTests.swift:323:74: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsScanTests.swift:344:71: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsScanTests.swift:372:86: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsScanTests.swift:375:68: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsScanTests.swift:409:86: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsScanTests.swift:515:71: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/RefsCoreTests/RefsScanTests.swift:95:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:96:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:97:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:98:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:99:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:100:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:101:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:110:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:111:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:112:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:113:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:114:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:115:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:124:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:125:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:126:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:142:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:143:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:144:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:157:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:158:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:159:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:160:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:170:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:171:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:172:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:173:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:174:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:188:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:188:52: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:189:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:190:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:191:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:285:40: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:285:49: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:286:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:287:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:312:40: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:312:49: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:313:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:314:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:331:40: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:331:50: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:332:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:333:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:342:40: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:342:50: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:343:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:344:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:345:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:346:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:355:40: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:355:50: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:356:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:357:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:357:15: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:358:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:359:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:389:40: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:389:50: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:390:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:391:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:442:40: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:442:50: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:443:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:444:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:445:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:446:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:461:40: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:461:49: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:462:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:463:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:489:40: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:489:50: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanTests.swift:490:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:491:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsScanTests.swift:534:26: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsScanReceiptTests.swift:42:270: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsRenameTests.swift:71:101: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsRenameTests.swift:226:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsRankingTests.swift:746:20: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsQuoteUnderlineTests.swift:200:66: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/RefsCoreTests/RefsPanelGeometryTests.swift:5:1: warning: [OrderedImports] place imports at the top of the file
Tests/RefsCoreTests/RefsPanelGeometryTests.swift:7:1: warning: [OrderedImports] place imports at the top of the file
Tests/RefsCoreTests/RefsPanelGeometryTests.swift:3:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/RefsCoreTests/RefsPanelGeometryTests.swift:12:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsPanelGeometryTests.swift:69:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsPDFUpdatesTests.swift:14:41: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsPDFUpdatesTests.swift:337:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsNewestTests.swift:76:21: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Tests/RefsCoreTests/RefsModelTests.swift:194:29: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsModelTests.swift:195:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsModelTests.swift:196:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsModelTests.swift:197:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsModelTests.swift:198:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsModelTests.swift:199:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsModelTests.swift:200:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsModelTests.swift:370:26: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsModelTests.swift:398:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsListScrollTests.swift:5:1: warning: [OrderedImports] place imports at the top of the file
Tests/RefsCoreTests/RefsListScrollTests.swift:7:1: warning: [OrderedImports] place imports at the top of the file
Tests/RefsCoreTests/RefsListScrollTests.swift:3:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/RefsCoreTests/RefsLinksTests.swift:336:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsLinksTests.swift:440:23: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsLinksTests.swift:441:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsLinksTests.swift:442:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsLinksTests.swift:505:14: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsLinksTests.swift:506:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsLinksTests.swift:507:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsLinksTests.swift:507:10: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsLinksTests.swift:571:14: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsLinksTests.swift:572:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsLinksTests.swift:573:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsLinksTests.swift:573:10: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsLinksTests.swift:628:14: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsLinksTests.swift:629:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsLinksTests.swift:630:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsLinksTests.swift:631:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsLinksTests.swift:631:10: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsLinksTests.swift:641:25: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsLinksTests.swift:642:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsLinksTests.swift:643:1: warning: [Indentation] indent by 4 spaces
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsInspectorTests.swift:87:78: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsInspectorTests.swift:370:79: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsInspectorTests.swift:775:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsInspectorTests.swift:948:46: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/RefsCoreTests/RefsInspectorTests.swift:88:38: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:89:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:90:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:158:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:159:1: warning: [Indentation] unindent by 11 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:160:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:161:1: warning: [Indentation] unindent by 11 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:390:47: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:391:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:392:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:396:47: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:397:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:398:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:402:46: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:403:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:404:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:485:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:485:57: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:486:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:487:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:814:14: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:815:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:816:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:817:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:817:14: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:896:20: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:921:38: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:922:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:923:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:931:23: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:932:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:933:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:937:38: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:938:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:939:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:954:37: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:955:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:956:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:958:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:960:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:961:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:962:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:992:37: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:993:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:994:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:995:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:996:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:997:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:998:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:999:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1000:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1010:37: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:1011:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1012:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1014:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1016:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1017:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1018:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1025:37: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:1026:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1027:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1036:22: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:1037:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1038:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1039:22: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:1040:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1041:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1047:37: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:1048:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1049:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1050:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1051:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1052:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1053:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1063:34: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:1064:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1065:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1068:35: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:1069:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1070:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1076:37: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:1077:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1078:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1086:22: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:1087:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1088:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsInspectorTests.swift:1169:26: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:1173:15: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsInspectorTests.swift:1180:26: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsImageMetricsTests.swift:5:1: warning: [OrderedImports] place imports at the top of the file
Tests/RefsCoreTests/RefsImageMetricsTests.swift:7:1: warning: [OrderedImports] place imports at the top of the file
Tests/RefsCoreTests/RefsImageMetricsTests.swift:3:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:553:15: warning: [ReplaceForEachWithForLoop] replace use of '.forEach { ... }' with for-in loop
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:243:26: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:278:71: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:419:46: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:463:73: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:102:23: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:103:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:104:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:105:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:106:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:107:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:108:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:109:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:110:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:111:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:112:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:113:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:114:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:115:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:115:14: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:144:23: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:145:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:146:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:147:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:148:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:149:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:150:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:151:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:151:14: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:166:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:178:23: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:179:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:180:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:181:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:188:23: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:188:53: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:188:66: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:189:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:190:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:191:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:192:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:193:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:194:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:195:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:196:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:196:90: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:197:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:198:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:199:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:199:15: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:219:23: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:219:37: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:220:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:221:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:222:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:223:23: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:223:36: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:224:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:225:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:226:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:227:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:228:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:229:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:244:22: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:245:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:245:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:246:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:252:23: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:252:36: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:253:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:254:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:255:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:256:23: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:256:37: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:257:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:258:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:264:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:268:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:271:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:279:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:310:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:310:47: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:311:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:312:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:313:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:314:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:315:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:316:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:375:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:376:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:384:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:424:23: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:424:29: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:424:42: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:425:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:426:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsHighlightsTabsTests.swift:426:15: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsFetchingTests.swift:311:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsFetchingTests.swift:328:103: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsFetchingTests.swift:356:103: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsFetchingTests.swift:377:96: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsFetchingTests.swift:535:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsDecodingTests.swift:48:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsDecodingTests.swift:49:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsDecodingTests.swift:50:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsDecodingTests.swift:63:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsDecodingTests.swift:64:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsDecodingTests.swift:65:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsDecodingTests.swift:66:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsDecodingTests.swift:67:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsDecodingTests.swift:76:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsDecodingTests.swift:77:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsDecodingTests.swift:78:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsDecodingTests.swift:79:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsDecodingTests.swift:129:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsDecodingTests.swift:130:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsDecodingTests.swift:131:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsDecodingTests.swift:167:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsDecodingTests.swift:168:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsDecodingTests.swift:169:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsDecodingTests.swift:203:26: warning: [AddLines] add 1 line break
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsCopyTests.swift:241:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsCopyTests.swift:435:47: warning: [TrailingComma] add trailing comma to the last element in multiline collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsCopyTests.swift:729:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsCopyTests.swift:817:83: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/RefsCoreTests/RefsCopyTests.swift:844:70: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/RefsCoreTests/RefsCopyTests.swift:9:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:10:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:11:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:23:45: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:23:63: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:24:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:25:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:26:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:26:14: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:42:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:75:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:85:31: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:85:53: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:86:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:87:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:88:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:89:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:90:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:92:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:94:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:103:31: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:103:45: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:104:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:105:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:106:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:107:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:129:24: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:129:41: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:130:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:131:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:139:32: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:140:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:141:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:161:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:209:33: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:209:47: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:210:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:211:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:212:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:213:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:214:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:224:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:226:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:240:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:261:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:269:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:275:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:281:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:289:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:291:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:312:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:314:43: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:315:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:316:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:334:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:335:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:336:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:337:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:338:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:339:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:340:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:341:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:342:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:343:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:345:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:346:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:359:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:360:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:361:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:429:28: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:429:40: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:429:54: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:430:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:431:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:455:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCopyTests.swift:459:34: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:459:48: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:460:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:461:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:487:34: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:487:48: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:488:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:489:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:490:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:513:34: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:513:48: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:514:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:515:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:516:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:631:31: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:631:55: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:632:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:633:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:634:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:635:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:636:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:637:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:638:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:648:33: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:648:47: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:649:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:650:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:651:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:652:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:653:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:736:28: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:736:40: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:736:54: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:737:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:738:1: warning: [Indentation] indent by 8 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:761:34: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:761:48: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCopyTests.swift:762:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyTests.swift:763:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCopyAlternatesTests.swift:89:100: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCodeTests.swift:25:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCodeTests.swift:35:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCodeTests.swift:104:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCodeTests.swift:112:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCodeTests.swift:125:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCodeTests.swift:146:23: warning: [AddLines] add 1 line break
Tests/RefsCoreTests/RefsCodeTests.swift:147:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCodeTests.swift:148:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCodeTests.swift:149:1: warning: [Indentation] indent by 4 spaces
Tests/RefsCoreTests/RefsCodeTests.swift:188:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCodeTests.swift:290:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCodeTests.swift:294:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCodeTests.swift:303:1: warning: [LineLength] line is too long
Tests/RefsCoreTests/RefsCodeTests.swift:304:1: warning: [LineLength] line is too long
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:229:27: warning: [TrailingComma] add trailing comma to the last element in multiline collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:351:33: warning: [TrailingComma] add trailing comma to the last element in multiline collection literal
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:164:100: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:192:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:193:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:194:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:228:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:278:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:345:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:355:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:356:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:357:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:358:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:359:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:476:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:477:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:478:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:525:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:526:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:527:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:528:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:529:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:530:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskLinkPickerPresentationTests.swift:558:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/TaskDisplayTextTests.swift:125:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/TaskDisplayTextTests.swift:153:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:272:100: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:273:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:302:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:315:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:316:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:317:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:328:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:329:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:330:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:331:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:332:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:358:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:359:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:360:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:361:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:362:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:363:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:364:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:365:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:366:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:367:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:368:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:369:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:370:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:379:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:380:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:386:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:387:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:388:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:389:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:390:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:391:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:392:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:393:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:394:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:395:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:396:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:410:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:410:31: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:411:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:412:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:413:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:414:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:415:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:416:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:417:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:418:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:419:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:438:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:469:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:471:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:498:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:499:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:500:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:501:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:502:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:503:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:504:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:505:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:509:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:510:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:511:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:512:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:513:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:514:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:515:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:516:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:518:94: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/TaskCompletePickerPresentationTests.swift:522:1: warning: [LineLength] line is too long
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/SimilarTasksBandPolicyTests.swift:30:79: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/SimilarTasksBandPolicyTests.swift:90:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:25:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:26:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:27:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:28:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:29:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:30:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:31:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:32:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:33:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:34:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:35:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:36:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:37:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:38:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:39:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:40:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:41:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:42:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:43:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:44:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:45:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:46:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:47:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:48:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:49:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:50:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:51:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:52:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:53:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:54:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:55:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:56:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:57:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:58:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:59:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:60:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:61:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:62:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:63:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:64:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:65:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:66:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:67:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:68:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:69:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:70:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:71:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:72:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:73:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:74:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:75:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:76:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:77:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:78:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:79:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:80:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:81:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:82:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:83:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:84:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:85:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:86:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:87:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:88:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:89:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:117:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:118:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:119:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:132:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:133:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:134:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ProjectTaskMovePickerPresentationTests.swift:142:1: warning: [LineLength] line is too long
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/PomodoroThemeSwatchesTests.swift:96:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/PomodoroThemeSwatchesTests.swift:230:79: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/CaptureCoreTests/PomodoroThemeSwatchesTests.swift:34:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/PomodoroThemeSwatchesTests.swift:34:33: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/PomodoroThemeSwatchesTests.swift:35:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/PomodoroThemeSwatchesTests.swift:36:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/PomodoroThemeSwatchesTests.swift:37:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/PomodoroThemeSwatchesTests.swift:46:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/PomodoroThemeSwatchesTests.swift:46:33: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/PomodoroThemeSwatchesTests.swift:47:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/PomodoroThemeSwatchesTests.swift:48:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/PomodoroThemeSwatchesTests.swift:49:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/PomodoroThemeSwatchesTests.swift:75:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/PomodoroThemeSwatchesTests.swift:75:33: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/PomodoroThemeSwatchesTests.swift:76:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/PomodoroThemeSwatchesTests.swift:77:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/PomodoroThemeSwatchesTests.swift:78:1: warning: [Indentation] indent by 4 spaces
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:277:27: warning: [TrailingComma] add trailing comma to the last element in multiline collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:468:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:492:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:179:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:180:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:181:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:182:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:183:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:184:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:185:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:186:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:187:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:188:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:189:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:190:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:191:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:192:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:193:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:194:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:195:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:196:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:197:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:198:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:199:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:200:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:201:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:202:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:203:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:204:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:205:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:206:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:207:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:208:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:209:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:210:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:211:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:212:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:276:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/ParentTaskPickerPresentationTests.swift:571:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/FuzzyMatcherTests.swift:109:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/FuzzyMatcherTests.swift:166:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:153:100: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:154:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:186:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:187:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:188:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:224:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:225:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:226:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:227:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:228:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:229:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:230:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:231:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:232:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:233:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:234:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:235:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:236:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:251:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:252:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:253:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:254:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:255:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:256:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:257:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:269:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:322:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:324:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/DependencyPickerPresentationTests.swift:513:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/DependencyDecodingTests.swift:12:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/DependencyDecodingTests.swift:13:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:14:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:15:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:16:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:17:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:18:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:19:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:20:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:21:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:22:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:23:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:24:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:25:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:26:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:27:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:28:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:41:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/DependencyDecodingTests.swift:42:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:43:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:44:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:45:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:46:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:47:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:48:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:49:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:50:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:51:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:52:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:53:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:66:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/DependencyDecodingTests.swift:67:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:68:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:69:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:70:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:71:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:72:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:73:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:74:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:75:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:76:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:77:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:78:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:79:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:90:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/DependencyDecodingTests.swift:91:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:92:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:93:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:94:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:95:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:96:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:97:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:98:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:99:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:100:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:101:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:102:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:103:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:104:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:105:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:106:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:107:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:108:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:122:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/DependencyDecodingTests.swift:123:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:124:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:125:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:126:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:127:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:128:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:129:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:130:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:131:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:132:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:133:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:134:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:135:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:136:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:137:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:138:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:139:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:140:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:141:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:142:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:143:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:144:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:145:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:146:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:147:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:148:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:183:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/DependencyDecodingTests.swift:191:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/DependencyDecodingTests.swift:192:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:193:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:194:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:195:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:196:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:197:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:198:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:211:48: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/DependencyDecodingTests.swift:212:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:213:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:214:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:215:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:216:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:217:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:218:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:219:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:220:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:221:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:222:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:223:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:224:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:225:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:226:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:227:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:228:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:229:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:230:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:231:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:232:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:233:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:234:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:235:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:236:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:237:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:238:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:239:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:240:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:241:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:242:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:243:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:244:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:262:48: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/DependencyDecodingTests.swift:263:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:264:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:265:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:266:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:267:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:268:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:269:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:270:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:271:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:362:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/DependencyDecodingTests.swift:391:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/DependencyDecodingTests.swift:402:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/DependencyDecodingTests.swift:403:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:404:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:405:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:406:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:407:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:408:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:409:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:410:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:527:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/DependencyDecodingTests.swift:528:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:529:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:530:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:531:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:532:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:533:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:695:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/DependencyDecodingTests.swift:696:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:697:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/DependencyDecodingTests.swift:698:1: warning: [Indentation] indent by 4 spaces
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CompletionRowContentTests.swift:506:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CompletionRowContentTests.swift:538:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CompletionRowContentTests.swift:565:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CompletionRowContentTests.swift:603:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CompletionRowContentTests.swift:624:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/CaptureCoreTests/CompletionRowContentTests.swift:345:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CompletionRowContentTests.swift:346:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CompletionRowContentTests.swift:347:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CompletionRowContentTests.swift:348:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CompletionRowContentTests.swift:349:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CompletionRowContentTests.swift:358:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CompletionRowContentTests.swift:359:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CompletionRowContentTests.swift:360:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CompletionRowContentTests.swift:677:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CompletionRowContentTests.swift:705:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CompletionRowContentTests.swift:731:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CompletionRowContentTests.swift:763:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CompletionRowContentTests.swift:792:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CompletionRowContentTests.swift:819:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CompletionRowContentTests.swift:1176:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CompletionRowContentTests.swift:1216:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CompletionRowContentTests.swift:1250:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CompletionRowContentTests.swift:1259:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CompletionRowContentTests.swift:1260:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CompletionRowContentTests.swift:1261:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CompletionRowContentTests.swift:1270:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CompletionRowContentTests.swift:1463:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CompletionRowContentTests.swift:1465:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CompletionRowContentTests.swift:1521:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CompletionRowContentTests.swift:1692:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:103:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:157:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:249:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:511:27: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:526:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:527:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:528:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:529:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:530:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:531:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:532:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:533:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:534:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:535:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:536:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:537:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:538:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:539:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:540:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:541:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:542:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:543:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:544:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:545:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:546:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:547:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:548:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:549:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:550:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:551:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:552:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:553:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:578:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:579:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:580:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:581:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:582:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:583:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:584:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:585:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:586:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:587:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:588:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:591:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:592:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:593:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:594:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:595:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:596:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:597:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:598:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:599:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:600:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:601:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:602:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:603:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:604:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:605:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:606:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:607:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:608:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:609:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:612:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:613:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:614:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:615:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:616:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:617:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:618:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:619:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:620:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:621:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:622:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:623:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:624:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:625:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:626:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:627:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:628:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:629:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:630:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:631:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:632:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:633:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:634:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:635:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:636:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:637:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:638:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:639:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:640:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:641:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:642:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:643:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:653:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:654:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:655:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:656:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:657:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:658:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:659:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:660:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:661:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:662:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:663:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:664:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:665:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:666:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:667:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:668:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:669:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:670:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:671:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:672:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:673:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:674:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:675:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:676:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:677:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:678:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:679:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTogglePresentationTests.swift:680:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTodayPomodoroGotoTests.swift:43:14: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureTodayPomodoroGotoTests.swift:44:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTodayPomodoroGotoTests.swift:45:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTodayPomodoroGotoTests.swift:45:10: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureTodayPomodoroGotoTests.swift:55:14: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureTodayPomodoroGotoTests.swift:56:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTodayPomodoroGotoTests.swift:57:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTodayPomodoroGotoTests.swift:57:10: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureTodayPomodoroGotoTests.swift:67:14: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureTodayPomodoroGotoTests.swift:68:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTodayPomodoroGotoTests.swift:69:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTodayPomodoroGotoTests.swift:69:10: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureTaskThemeTests.swift:270:20: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureTaskThemeTests.swift:275:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTaskThemeTests.swift:276:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTaskThemeTests.swift:277:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTaskThemeTests.swift:278:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTaskThemeTests.swift:279:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTaskThemeTests.swift:280:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTaskThemeTests.swift:281:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTaskThemeTests.swift:282:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTaskThemeTests.swift:283:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTaskThemeTests.swift:284:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTaskCompletePresentationTests.swift:162:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureTaskCompletePresentationTests.swift:165:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureTaskCompletePresentationTests.swift:312:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureTaskCompletePresentationTests.swift:412:1: warning: [LineLength] line is too long
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureTaskBlockPresentationTests.swift:404:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureTaskBlockPresentationTests.swift:430:75: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureTaskBlockPresentationTests.swift:464:85: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/CaptureCoreTests/CaptureTaskBlockPresentationTests.swift:169:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureTaskBlockPresentationTests.swift:228:15: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureTaskBlockPresentationTests.swift:229:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTaskBlockPresentationTests.swift:230:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTaskBlockPresentationTests.swift:231:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTaskBlockPresentationTests.swift:232:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTaskBlockPresentationTests.swift:233:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTaskBlockPresentationTests.swift:234:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTaskBlockPresentationTests.swift:298:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureTaskBlockPresentationTests.swift:299:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTaskBlockPresentationTests.swift:300:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureTaskBlockPresentationTests.swift:301:1: warning: [Indentation] indent by 4 spaces
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:224:79: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:351:22: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:130:20: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:131:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:132:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:133:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:134:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:134:14: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:140:20: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:141:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:142:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:143:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:144:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:145:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:145:14: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:150:20: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:151:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:152:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:153:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:154:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:154:14: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:249:23: warning: [Spacing] remove 1 space
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:249:27: warning: [Spacing] remove 1 space
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:282:33: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:283:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:284:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:285:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorPresentationTests.swift:286:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorOfferRowsTests.swift:115:14: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureSuccessorOfferRowsTests.swift:116:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorOfferRowsTests.swift:117:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorOfferRowsTests.swift:118:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorOfferRowsTests.swift:118:10: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureSuccessorOfferRowsTests.swift:153:14: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureSuccessorOfferRowsTests.swift:154:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorOfferRowsTests.swift:155:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorOfferRowsTests.swift:156:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureSuccessorOfferRowsTests.swift:156:10: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureSavedTemplatesTests.swift:453:20: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Tests/CaptureCoreTests/CaptureSavedTemplatesTests.swift:120:102: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureSavedTemplatesTests.swift:204:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureSavedTemplatesTests.swift:241:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureSavedTemplatesTests.swift:269:102: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureSavedTemplatesTests.swift:338:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureSavedTemplatesTests.swift:507:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureSavedTemplatesTests.swift:510:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureSavedTemplatesTests.swift:513:1: warning: [LineLength] line is too long
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:97:117: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:56:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:56:47: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:57:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:58:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:59:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:92:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:92:53: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:93:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:94:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:105:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:106:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:107:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:108:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:109:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:255:1: warning: [Indentation] unindent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:255:49: warning: [RemoveLine] remove line break
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:347:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:348:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:349:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:350:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipPresentationTests.swift:351:1: warning: [Indentation] indent by 4 spaces
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureRelationshipCopyTests.swift:126:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureRelationshipCopyTests.swift:140:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/CaptureCoreTests/CaptureRelationshipCopyTests.swift:63:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureRelationshipCopyTests.swift:212:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRelationshipCopyTests.swift:213:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipCopyTests.swift:214:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipCopyTests.swift:215:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipCopyTests.swift:216:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipCopyTests.swift:217:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipCopyTests.swift:218:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipCopyTests.swift:219:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipCopyTests.swift:220:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipCopyTests.swift:221:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipCopyTests.swift:222:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationshipCopyTests.swift:223:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationSuccessorPresentationTests.swift:97:2: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:14:18: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:15:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:16:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:17:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:17:14: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:26:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:56:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:57:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:58:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:59:14: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:60:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:61:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:62:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:62:10: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:93:34: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:94:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:95:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:143:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:159:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:188:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:200:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:202:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:219:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:229:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureRelationSuccessorDecodingTests.swift:240:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureRelationHeldPresentationTests.swift:41:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureRelationHeldPresentationTests.swift:43:96: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRelationHeldPresentationTests.swift:169:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationHeldPresentationTests.swift:170:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:155:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:166:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:506:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:507:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:508:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:509:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:510:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:511:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:512:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:513:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:514:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:515:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:516:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:519:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:520:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:521:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:522:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:523:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:524:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:525:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:526:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:527:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:528:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:529:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:530:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:531:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:532:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:533:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:534:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:535:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:536:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:537:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:538:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:539:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:540:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:541:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:542:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:543:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:544:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:545:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:546:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:547:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:548:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:549:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:552:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:553:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:554:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:555:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:556:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:557:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:558:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:559:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:560:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:561:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:562:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:563:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:564:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:565:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:566:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:567:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:568:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:569:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:570:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:571:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:572:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:573:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:574:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:575:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:578:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:579:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:580:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:581:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:582:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:583:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:584:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:585:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:586:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:587:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:588:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:589:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:590:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:591:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:592:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:595:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:596:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:597:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:598:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:599:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:600:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:601:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:602:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:603:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:604:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:605:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:606:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:607:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:608:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:609:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:610:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:611:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:612:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:613:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:614:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:615:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:616:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:617:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:618:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:619:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:620:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:621:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:622:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:623:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:624:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:625:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:626:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:627:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:628:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:629:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:630:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:631:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:632:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:633:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:634:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:635:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:636:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:637:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:638:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:641:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:642:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:643:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:644:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:645:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:646:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:647:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:648:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:649:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:650:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:651:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:652:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:653:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:654:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:655:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:656:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:657:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:658:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:659:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:660:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:661:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:662:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:663:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:664:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:665:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:666:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:667:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:668:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:669:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:670:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:671:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:672:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:673:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:674:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:675:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:676:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:677:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:678:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:679:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:680:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:681:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:682:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:683:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCompleteTests.swift:684:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:147:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:413:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:414:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:415:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:416:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:417:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:418:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:419:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:420:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:421:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:422:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:423:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:426:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:427:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:428:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:429:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:430:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:431:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:432:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:433:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:434:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:435:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:436:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:437:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:438:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:439:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:440:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:441:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:442:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:443:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:444:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:445:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:446:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:447:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:448:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:449:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:450:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:451:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:452:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:453:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:454:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:455:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:456:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:459:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:460:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:461:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:462:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:463:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:464:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:465:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:466:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:467:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:468:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:469:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:470:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:471:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:472:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:473:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:474:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:475:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:476:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:477:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:478:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:479:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:480:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:481:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:482:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:485:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:486:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:487:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:488:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:489:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:490:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:491:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:492:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:493:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:494:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:495:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:496:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:497:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:498:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:499:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:502:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:503:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:504:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:505:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:506:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:507:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:508:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:509:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:510:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:511:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:512:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:513:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:514:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:515:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:516:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:517:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:518:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:519:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:520:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:521:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:522:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:523:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:524:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:525:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:526:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:527:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:528:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:529:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:530:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:531:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:532:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:533:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:534:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:537:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:538:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:539:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:540:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:541:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:542:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:543:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:544:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:545:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:546:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:547:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:548:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:549:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:550:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:551:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:552:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:553:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:554:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:555:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:556:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:557:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:558:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:559:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:560:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:561:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:562:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:563:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:564:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:565:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:566:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:567:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:568:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:569:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:570:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:571:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:572:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:573:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:574:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:575:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:576:1: warning: [Indentation] replace leading whitespace with 4 spaces
Tests/CaptureCoreTests/CaptureRelationCancelTests.swift:577:1: warning: [Indentation] replace leading whitespace with 4 spaces
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureRelatedModelsTests.swift:49:73: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/CaptureCoreTests/CaptureRelatedModelsTests.swift:46:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRelatedModelsTests.swift:46:51: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRelatedModelsTests.swift:47:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelatedModelsTests.swift:48:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRelatedModelsTests.swift:59:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureRefPresentationTests.swift:590:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureRefPresentationTests.swift:591:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:37:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:38:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:39:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:40:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:41:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:42:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:43:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:48:27: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:49:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:50:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:51:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:52:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:53:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:54:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:60:28: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:61:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:62:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:63:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:64:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:65:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:66:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:72:28: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:73:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:74:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:75:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:76:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:77:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:78:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:83:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:84:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:85:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:86:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:87:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:88:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:89:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:90:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:91:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:92:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:93:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:94:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:95:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:96:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:97:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:98:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:99:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:100:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:101:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:102:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:103:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:104:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:105:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:106:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:107:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:108:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:109:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureRefFileUnderTests.swift:110:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePullInDecodingTests.swift:74:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePullInDecodingTests.swift:80:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePullInDecodingTests.swift:93:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePullInDecodingTests.swift:103:14: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePullInDecodingTests.swift:104:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePullInDecodingTests.swift:105:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePullInDecodingTests.swift:106:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePullInDecodingTests.swift:106:10: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePullInDecodingTests.swift:128:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePullInDecodingTests.swift:129:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePullInDecodingTests.swift:133:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePullInDecodingTests.swift:150:14: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePullInDecodingTests.swift:151:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePullInDecodingTests.swift:152:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePullInDecodingTests.swift:153:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePullInDecodingTests.swift:153:10: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePullInClientTests.swift:30:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePullInClientTests.swift:45:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePullInClientTests.swift:49:100: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePullInClientTests.swift:86:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePullInClientTests.swift:93:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePullInClientTests.swift:113:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePullInClientTests.swift:137:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePullInClientTests.swift:145:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePullInClientTests.swift:151:14: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePullInClientTests.swift:152:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePullInClientTests.swift:153:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePullInClientTests.swift:154:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePullInClientTests.swift:154:10: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePullInClientTests.swift:158:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePullInClientTests.swift:165:14: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePullInClientTests.swift:166:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePullInClientTests.swift:167:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePullInClientTests.swift:168:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePullInClientTests.swift:168:10: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePullInClientTests.swift:172:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePullInClientTests.swift:193:1: warning: [LineLength] line is too long
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureProjectNotePresentationTests.swift:117:67: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/CaptureCoreTests/CaptureProjectNotePresentationTests.swift:80:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureProjectNotePresentationTests.swift:81:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureProjectNotePresentationTests.swift:82:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureProjectNotePresentationTests.swift:110:22: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureProjectNotePresentationTests.swift:111:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureProjectNotePresentationTests.swift:112:1: warning: [Indentation] indent by 4 spaces
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureProjectNoteMovePresentationTests.swift:391:91: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:435:39: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:139:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:218:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:232:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:298:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:514:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:525:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:540:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:618:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:652:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:669:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:772:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:773:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:774:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:775:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:914:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:997:1: warning: [Indentation] indent by 2 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1094:1: warning: [Indentation] indent by 2 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1107:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1210:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1211:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1212:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1213:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1214:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1230:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1231:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1232:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1233:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1234:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1235:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1236:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1237:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1238:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1239:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1240:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1241:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1242:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1243:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1244:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1245:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1246:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1247:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1248:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1249:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1250:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1251:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1252:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1253:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1254:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1255:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1256:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1262:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1263:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1264:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1265:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1266:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1267:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1268:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1269:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1270:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1271:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1272:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1273:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1274:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1275:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1276:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1277:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1278:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1279:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1280:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1281:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1282:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1283:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1284:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1285:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1286:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1287:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroStartPresentationTests.swift:1288:1: warning: [Indentation] indent by 4 spaces
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePomodoroLineTokensTests.swift:198:60: warning: [TrailingComma] add trailing comma to the last element in multiline collection literal
Tests/CaptureCoreTests/CapturePomodoroLineTokensTests.swift:199:14: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePomodoroLineTokensTests.swift:200:1: warning: [Indentation] indent by 3 spaces
Tests/CaptureCoreTests/CapturePomodoroLineTokensTests.swift:200:57: warning: [AddLines] add 1 line break
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1009:42: warning: [TrailingComma] add trailing comma to the last element in multiline collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1126:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1264:56: warning: [TrailingComma] add trailing comma to the last element in multiline collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1355:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1402:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1525:53: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1527:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1537:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1569:46: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1571:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1604:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1633:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1657:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1741:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:160:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:178:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:182:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:189:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:782:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:973:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1002:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1083:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1084:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1085:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1164:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1165:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1166:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1171:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1172:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1173:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1239:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1253:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1254:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1255:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1259:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1261:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1262:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1302:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1459:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1460:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1461:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1466:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1467:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1468:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1472:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1473:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1474:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1475:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1476:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1477:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1843:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1854:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1859:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePomodoroClosePresentationTests.swift:1874:1: warning: [LineLength] line is too long
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePomodoroBlockPresentationTests.swift:339:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/CaptureCoreTests/CapturePlanBudgetPresentationTests.swift:147:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePlanBudgetPresentationTests.swift:148:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePlanBudgetPresentationTests.swift:149:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePlanBudgetPresentationTests.swift:150:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePlanBudgetPresentationTests.swift:150:14: warning: [AddLines] add 1 line break
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:113:32: warning: [TrailingComma] add trailing comma to the last element in multiline collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:128:59: warning: [TrailingComma] add trailing comma to the last element in multiline collection literal
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:42:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:43:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:44:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:45:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:46:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:47:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:48:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:49:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:50:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:51:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:52:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:53:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:54:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:55:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:57:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:70:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:70:60: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:71:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:72:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:73:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:74:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:77:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:89:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CapturePickerPresentationTests.swift:227:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:50:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:51:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:52:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:77:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:135:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:136:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:137:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:138:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:139:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:140:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:141:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:142:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:143:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:144:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:145:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:146:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:147:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:148:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:166:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:167:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:173:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:179:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:180:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:181:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:182:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:183:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureOpenPlanTests.swift:184:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureModelTests.swift:480:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureModelTests.swift:788:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureModelTests.swift:1043:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureModelTests.swift:2153:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureModelTests.swift:2196:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureModelTests.swift:2197:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureInboxRouteStateTests.swift:133:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureInboxRouteClientTests.swift:17:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureInboxRouteClientTests.swift:184:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureInboxRouteClientTests.swift:233:1: warning: [LineLength] line is too long
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:126:69: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:159:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:209:69: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:215:65: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:257:63: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:267:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:273:76: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:465:23: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:486:82: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:503:26: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:504:23: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:530:83: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:554:83: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:602:83: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:618:100: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:619:27: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:640:26: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:641:23: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:652:81: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:663:69: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:677:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:721:86: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:735:76: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:744:69: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:858:34: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:863:34: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:865:26: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:870:88: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:875:86: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:943:68: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:124:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:125:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:126:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:153:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:154:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:155:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:156:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:157:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:158:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:160:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:161:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:175:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:176:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:177:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:178:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:202:29: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:203:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:204:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:249:29: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:250:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:251:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:254:31: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:255:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:256:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:257:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:258:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:259:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:260:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:263:32: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:264:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:265:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:284:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:285:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:286:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:287:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:288:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:289:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:290:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:291:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:303:31: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:304:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:305:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:306:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:310:38: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:311:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:312:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:313:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:341:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:342:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:343:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:344:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:345:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:346:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:347:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:355:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:356:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:357:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:358:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:388:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:389:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:390:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:391:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:392:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:401:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:402:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:403:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:404:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:442:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:443:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:443:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:443:44: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:444:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:445:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:446:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:447:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:455:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:456:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:457:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:458:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:464:30: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:465:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:466:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:473:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:474:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:474:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:474:31: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:475:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:476:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:477:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:478:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:479:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:480:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:481:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:504:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:505:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:506:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:527:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:528:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:529:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:574:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:575:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:576:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:586:40: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:587:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:587:27: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:587:35: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:588:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:589:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:590:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:598:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:599:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:599:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:599:31: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:600:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:601:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:602:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:603:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:604:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:605:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:606:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:607:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:608:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:609:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:617:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:618:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:619:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:627:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:628:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:629:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:636:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:637:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:638:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:639:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:640:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:641:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:642:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:653:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:654:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:655:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:656:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:663:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:664:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:665:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:666:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:672:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:673:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:673:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:673:31: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:674:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:675:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:676:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:677:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:677:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:677:59: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:678:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:679:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:680:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:690:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:691:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:692:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:698:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:699:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:700:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:802:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:803:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:803:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:803:44: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:804:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:805:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:806:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:807:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:808:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:809:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:810:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:811:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:812:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:813:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:814:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:815:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:816:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:817:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:818:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:819:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:819:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:819:59: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:820:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:821:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:822:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:822:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:822:61: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:823:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:824:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:825:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:874:36: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:875:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:875:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:875:44: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:876:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:877:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:878:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:879:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:880:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:881:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:882:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:883:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:884:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:885:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:885:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:885:59: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:886:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:887:1: warning: [Indentation] indent by 8 spaces
Tests/CaptureCoreTests/CaptureAgendaPresentationTests.swift:888:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:126:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:127:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:128:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:129:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:130:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:131:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:132:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:133:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:134:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:135:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:136:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:163:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:164:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:165:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:166:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:167:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:168:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:169:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:170:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:171:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:172:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:173:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:174:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:175:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:176:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:177:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:178:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:179:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:180:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:181:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:182:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:183:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:184:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:185:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:186:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:187:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:188:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:189:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:190:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:191:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:192:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:218:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:219:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:220:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:221:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:222:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:223:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:224:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:231:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaModelsTests.swift:232:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:80:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:80:56: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:81:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:82:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:122:1: warning: [Indentation] indent by 2 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:149:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:150:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:151:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:152:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:153:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:154:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:155:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:156:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:157:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:158:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:159:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:160:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:161:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:162:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:163:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:164:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:165:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:166:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:167:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:168:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:169:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:170:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:171:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:172:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaHomesTests.swift:173:1: warning: [Indentation] indent by 4 spaces
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:109:26: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:121:26: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:133:26: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:145:26: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:285:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:316:22: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:332:61: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:337:62: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:99:26: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:100:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:101:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:102:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:103:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:104:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:105:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:106:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:107:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:108:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:109:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:110:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:111:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:112:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:113:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:114:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:115:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:116:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:117:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:118:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:119:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:120:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:121:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:122:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:123:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:124:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:125:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:126:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:127:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:128:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:129:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:130:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:131:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:132:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:133:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:134:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:135:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:136:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:137:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:138:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:139:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:140:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:141:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:142:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:143:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:144:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:145:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:146:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:147:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:148:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:278:25: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:279:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:280:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:281:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:282:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:283:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:283:18: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:308:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:308:60: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:309:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:314:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:326:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:326:60: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:327:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:328:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:329:23: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:329:59: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:330:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaFitPlannerTests.swift:331:1: warning: [Indentation] indent by 4 spaces
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:220:83: warning: [TrailingComma] add trailing comma to the last element in multiline collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:242:63: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:281:63: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:289:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:312:48: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:328:48: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:339:48: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:202:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:202:30: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:203:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:204:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:205:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:211:33: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:212:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:212:21: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:213:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:214:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:214:21: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:215:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:216:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:235:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:273:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:303:25: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:318:25: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CaptureAgendaCalendarTests.swift:328:25: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/CanceledDraftStashStoreTests.swift:14:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CanceledDraftStashStoreTests.swift:24:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CanceledDraftStashStoreTests.swift:87:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CanceledDraftStashStoreTests.swift:96:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CanceledDraftStashStoreTests.swift:111:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CanceledDraftStashStoreTests.swift:124:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/CanceledDraftStashStoreTests.swift:172:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:110:1: warning: [Indentation] indent by 1 spaces
Tests/CaptureCoreTests/BobProcessClientTests.swift:305:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:333:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:363:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:385:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:417:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:467:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:468:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:500:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:530:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:561:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:587:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:647:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:727:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:802:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:810:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:973:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:1251:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:1449:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:1472:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:1478:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:1483:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:1515:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:1527:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:1563:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:1604:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:1635:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:1653:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:1675:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:1694:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:1892:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobProcessClientTests.swift:2340:26: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/BobProcessClientTests.swift:2344:15: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/BobExecutableResolverTests.swift:12:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BobExecutableResolverTests.swift:33:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BlockIDRulesTests.swift:160:1: warning: [NoAccessLevelOnExtensionDeclaration] remove this 'private' access modifier and declare each member inside this extension as 'fileprivate'
Tests/CaptureCoreTests/BlockIDRulesTests.swift:161:5: note: add 'fileprivate' access modifier to this declaration
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/BlockIDPickerIndexTests.swift:141:69: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/CaptureCoreTests/BlockIDPickerIndexTests.swift:213:82: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/CaptureCoreTests/BlockIDPickerIndexTests.swift:106:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BlockIDPickerIndexTests.swift:107:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BlockIDPickerIndexTests.swift:108:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BlockIDPickerIndexTests.swift:130:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BlockIDPickerIndexTests.swift:153:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BlockIDPickerIndexTests.swift:172:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BlockIDPickerIndexTests.swift:358:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/BlockIDPickerIndexTests.swift:358:51: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/BlockIDPickerIndexTests.swift:359:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/BlockIDPickerIndexTests.swift:360:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/BlockIDPickerIndexTests.swift:380:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BlockIDPickerIndexTests.swift:436:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BlockIDPickerIndexTests.swift:642:1: warning: [LineLength] line is too long
Tests/CaptureCoreTests/BlockIDDecodingTests.swift:62:24: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/BlockIDDecodingTests.swift:62:49: warning: [AddLines] add 1 line break
Tests/CaptureCoreTests/BlockIDDecodingTests.swift:63:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/BlockIDDecodingTests.swift:64:1: warning: [Indentation] indent by 4 spaces
Tests/CaptureCoreTests/BlockIDDecodingTests.swift:65:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/TaskCompleteDesignTests.swift:18:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/TaskCompleteDesignTests.swift:20:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/TaskCompleteDesignTests.swift:84:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/TaskCompleteDesignTests.swift:85:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/TaskBlockDesignTests.swift:22:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/TaskBlockDesignTests.swift:85:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/TaskBlockDesignTests.swift:86:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/StatusItemGlyphDesignTests.swift:20:14: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/StatusItemGlyphDesignTests.swift:21:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/StatusItemGlyphDesignTests.swift:22:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/StatusItemGlyphDesignTests.swift:22:30: warning: [AddLines] add 1 line break
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/SimilarTasksBandDesignTests.swift:66:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/SimilarTasksBandDesignTests.swift:112:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/SimilarTasksBandDesignTests.swift:137:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/SimilarTasksBandDesignTests.swift:158:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/SimilarTasksBandDesignTests.swift:179:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/SimilarTasksBandDesignTests.swift:204:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/SimilarTasksBandDesignTests.swift:226:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/SimilarTasksBandDesignTests.swift:299:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/SimilarTasksBandDesignTests.swift:331:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/BobMacCaptureTests/SimilarTasksBandDesignTests.swift:34:54: warning: [AddLines] add 1 line break
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/SimilarTasksActionsTests.swift:85:77: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/SimilarTasksActionsTests.swift:105:74: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/SimilarTasksActionsTests.swift:184:77: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/SimilarTasksActionsTests.swift:204:77: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/BobMacCaptureTests/SimilarTasksActionsTests.swift:269:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RenderFixtureWriter.swift:22:14: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RenderFixtureWriter.swift:23:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RenderFixtureWriter.swift:24:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RenderFixtureWriter.swift:24:30: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:23:29: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:24:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:25:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:26:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:27:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:28:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:41:21: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:42:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:43:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:47:24: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:48:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:49:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:63:46: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:64:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:65:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:95:39: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:96:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:97:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:118:27: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:119:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:120:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:121:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:122:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:123:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:124:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:125:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:126:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:127:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:128:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:129:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:130:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:131:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:132:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsTodayLinkCardDesignTests.swift:133:1: warning: [Indentation] indent by 4 spaces
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/RefsPanelModelTests.swift:2973:51: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4183:87: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:283:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:495:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:710:85: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:1433:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:1557:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:1639:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:1703:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:1757:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:2438:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:3616:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:3618:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:3634:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:3636:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4047:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4069:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4108:30: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4109:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4109:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4110:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4118:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4143:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4148:30: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4149:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4155:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4167:25: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4168:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4169:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4169:15: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4182:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4489:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:4499:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:5012:30: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:5013:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:5014:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:5045:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:5065:30: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:5066:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:5067:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:6077:30: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:6077:40: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:6078:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:7008:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:7467:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:7486:95: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsPanelModelTests.swift:7506:91: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsPanelDesignTests.swift:678:100: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsPanelDesignTests.swift:790:101: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsKeyRouterTests.swift:448:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsKeyRouterTests.swift:449:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsInspectorScrollTests.swift:66:22: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsInspectorScrollTests.swift:67:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsInspectorScrollTests.swift:68:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsInspectorScrollTests.swift:69:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/RefsInspectorScrollTests.swift:472:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/RefsCopyComponentsTests.swift:189:2: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsCopyCardDesignTests.swift:96:1: warning: [Indentation] unindent by 4 spaces
Tests/BobMacCaptureTests/RefsCopyCardDesignTests.swift:821:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/RefsCopyCardDesignTests.swift:833:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/PomodoroCloseDesignTests.swift:24:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/PomodoroCloseDesignTests.swift:86:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/PomodoroCloseDesignTests.swift:87:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/PomodoroBlockDesignTests.swift:23:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/PomodoroBlockDesignTests.swift:25:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/PomodoroBlockDesignTests.swift:87:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/PomodoroBlockDesignTests.swift:88:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/PomodoroBlockDesignTests.swift:93:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:405:14: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:119:19: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:120:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:121:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:122:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:123:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:124:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:125:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:126:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:127:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:128:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:129:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:130:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:131:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:132:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:133:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:134:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:135:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:136:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:137:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:138:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:139:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:140:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:141:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:142:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:143:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:144:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:145:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:146:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:147:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:148:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:149:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:150:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:151:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:152:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:153:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:154:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:155:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:156:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:157:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:158:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:159:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:160:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:161:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:162:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:163:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:164:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:165:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:166:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:167:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:168:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:169:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:170:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:171:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:172:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:173:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/PlainTextPasteTests.swift:319:1: warning: [LineLength] line is too long
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:19:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:77:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:124:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:154:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:217:26: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:234:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:281:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:353:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:436:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:502:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:517:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:532:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:568:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:594:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:633:26: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:642:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:786:101: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:798:67: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:817:72: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:836:83: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:861:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:877:63: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:895:73: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:927:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:961:68: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:1300:80: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:1548:74: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:1573:74: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:1863:22: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:1964:22: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/NotificationServiceTests.swift:2106:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/BobMacCaptureTests/NotificationServiceTests.swift:29:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:165:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:292:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:359:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:376:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:401:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:437:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:442:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:663:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:695:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:721:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:754:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:762:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:768:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:789:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:806:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:819:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:843:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:859:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:873:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:925:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:934:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:950:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:977:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:982:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:984:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:985:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:989:17: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/NotificationServiceTests.swift:990:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/NotificationServiceTests.swift:991:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/NotificationServiceTests.swift:992:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/NotificationServiceTests.swift:993:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/NotificationServiceTests.swift:994:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/NotificationServiceTests.swift:994:97: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/NotificationServiceTests.swift:1023:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:1040:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:1297:24: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/NotificationServiceTests.swift:1298:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/NotificationServiceTests.swift:1299:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/NotificationServiceTests.swift:1300:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/NotificationServiceTests.swift:1301:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/NotificationServiceTests.swift:1301:14: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/NotificationServiceTests.swift:1550:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:1552:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:1553:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:1604:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:1640:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:1681:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/NotificationServiceTests.swift:2209:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/HotKeyRegistryTests.swift:110:39: warning: [GroupNumericLiterals] group every 4 digits in this hexadecimal literal using a '_' separator
Tests/BobMacCaptureTests/CaptureUnconfiguredThemeHostedTests.swift:95:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureUnconfiguredThemeHostedTests.swift:99:15: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureTodayPomodoroPanelTests.swift:210:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureTodayPomodoroPanelTests.swift:214:15: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureTemplateShelfModelTests.swift:30:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTemplateShelfModelTests.swift:145:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTemplateShelfModelTests.swift:349:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTemplateShelfModelTests.swift:356:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTemplateShelfModelTests.swift:462:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTemplateShelfModelTests.swift:477:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTemplateShelfModelTests.swift:520:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTemplateShelfModelTests.swift:539:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTemplateShelfModelTests.swift:550:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTemplateShelfModelTests.swift:569:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTemplateShelfModelTests.swift:616:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTemplateShelfModelTests.swift:652:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTemplateShelfDesignTests.swift:34:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTemplatePresentationTests.swift:45:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTemplatePresentationTests.swift:60:14: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureTemplatePresentationTests.swift:61:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureTemplatePresentationTests.swift:62:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureTemplatePresentationTests.swift:62:28: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureTemplatePresentationTests.swift:63:1: warning: [LineLength] line is too long
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CaptureTaskTypeHostedTests.swift:13:86: warning: [TrailingComma] add trailing comma to the last element in multiline collection literal
Tests/BobMacCaptureTests/CaptureTaskTypeHostedTests.swift:14:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTaskLinkPanelTests.swift:68:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTaskLinkPanelTests.swift:79:1: warning: [LineLength] line is too long
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CaptureTaskGotoPanelTests.swift:170:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/BobMacCaptureTests/CaptureTaskGotoPanelTests.swift:445:18: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureTaskGotoPanelTests.swift:445:28: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureTaskGotoPanelTests.swift:464:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureTaskGotoPanelTests.swift:468:15: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureTaskCompletePanelTests.swift:27:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTaskCompletePanelTests.swift:62:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTaskCompletePanelTests.swift:100:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTaskCompletePanelTests.swift:261:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTaskCompletePanelTests.swift:262:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureTaskCompletePanelTests.swift:341:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureTaskCompletePanelTests.swift:345:15: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureTargetsRefreshGateTests.swift:48:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:78:24: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:136:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:140:15: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:266:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:284:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:543:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:592:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:657:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:666:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:676:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:685:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:697:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:714:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:746:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:766:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:829:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:848:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:849:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:869:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:881:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:917:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:938:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:956:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:964:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:983:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:986:101: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:996:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:1015:101: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:1041:101: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureSeparatorToggleTests.swift:1063:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureSavedTemplateShelfTests.swift:108:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:29:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:45:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:452:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:453:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:454:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:455:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:456:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:457:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:509:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:513:15: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1138:101: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1138:112: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1419:23: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1420:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1421:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1583:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1653:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1654:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1655:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1656:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1657:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1658:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1659:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1660:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1661:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1662:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1663:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1664:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1665:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1666:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1667:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1668:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1669:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1670:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1671:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1672:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1874:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1884:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1885:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1886:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1887:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1888:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1889:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1890:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1891:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1892:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1893:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1894:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1895:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1896:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1897:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1898:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1899:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1900:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1901:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1902:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1903:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1904:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1905:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1906:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1907:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1908:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1909:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1910:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1911:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1912:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1913:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1926:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1927:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1928:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1929:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1930:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1931:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1932:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1933:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1934:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1935:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1936:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1937:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1938:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1939:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1940:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1941:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1942:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1943:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1944:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1945:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1946:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1947:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1948:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1949:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1950:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1951:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1952:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1953:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1954:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1955:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1956:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1957:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1958:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1959:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1960:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1961:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1962:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1963:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1964:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1965:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1966:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:1967:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureRelatedLaneTests.swift:61:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureRelatedLaneTests.swift:65:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureRelatedLaneTests.swift:113:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureRelatedLaneTests.swift:149:19: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureRelatedLaneTests.swift:151:1: warning: [LineLength] line is too long
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CaptureRefPanelTests.swift:95:53: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CaptureRefPanelTests.swift:105:57: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/BobMacCaptureTests/CaptureRefPanelTests.swift:151:15: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePullInChoiceTests.swift:745:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePullInChoiceTests.swift:751:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePullInChoiceTests.swift:752:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePullInChoiceDesignTests.swift:209:14: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePullInChoiceDesignTests.swift:210:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePullInChoiceDesignTests.swift:211:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePullInChoiceDesignTests.swift:212:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePullInChoiceDesignTests.swift:213:1: warning: [Indentation] indent by 1 spaces
Tests/BobMacCaptureTests/CapturePullInChoiceDesignTests.swift:214:1: warning: [Indentation] indent by 1 spaces
Tests/BobMacCaptureTests/CapturePullInChoiceDesignTests.swift:215:1: warning: [Indentation] indent by 1 spaces
Tests/BobMacCaptureTests/CapturePullInChoiceDesignTests.swift:216:1: warning: [Indentation] indent by 1 spaces
Tests/BobMacCaptureTests/CapturePreviewFullHeightTests.swift:16:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePreviewFullHeightTests.swift:21:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePreviewFullHeightTests.swift:192:27: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePreviewFullHeightTests.swift:193:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePreviewFullHeightTests.swift:194:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePreviewFullHeightTests.swift:195:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePreviewFullHeightTests.swift:320:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePreviewFullHeightTests.swift:322:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePreviewFullHeightTests.swift:323:1: warning: [Indentation] unindent by 4 spaces
Tests/BobMacCaptureTests/CapturePreviewFullHeightTests.swift:345:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePreviewFullHeightTests.swift:355:1: warning: [LineLength] line is too long
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePickerMarkerHighlightTests.swift:193:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:432:82: warning: [TrailingComma] add trailing comma to the last element in multiline collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:482:82: warning: [TrailingComma] add trailing comma to the last element in multiline collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:1090:14: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:1324:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:67:27: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:72:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:75:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:76:1: warning: [Indentation] unindent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:139:27: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:144:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:145:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:146:1: warning: [Indentation] unindent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:198:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:199:1: warning: [Indentation] unindent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:381:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:422:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:423:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:424:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:425:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:426:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:427:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:428:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:428:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:429:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:430:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:431:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:432:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:433:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:434:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:435:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:436:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:437:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:438:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:439:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:440:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:441:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:442:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:443:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:444:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:445:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:446:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:447:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:448:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:449:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:450:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:451:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:452:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:453:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:454:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:455:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:456:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:457:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:458:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:459:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:460:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:461:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:462:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:463:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:464:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:465:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:466:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:467:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:468:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:469:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:470:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:471:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:472:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:473:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:474:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:475:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:476:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:476:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:477:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:478:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:479:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:480:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:481:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:482:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:483:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:484:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:485:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:486:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:487:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:488:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:489:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:490:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:491:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:492:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:493:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:494:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:495:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:637:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:638:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:638:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:639:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:639:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:640:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:641:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:676:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:677:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:678:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:679:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:722:101: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:723:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:724:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:724:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:725:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:726:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:727:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:728:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:729:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:730:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:774:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:939:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:940:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:1077:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:1168:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:1244:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:1261:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:1278:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePickerDesignTests.swift:1306:1: warning: [LineLength] line is too long
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CaptureParentTaskPanelTests.swift:557:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/BobMacCaptureTests/CaptureParentTaskPanelTests.swift:355:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureParentTaskPanelTests.swift:381:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureParentTaskPanelTests.swift:449:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureParentTaskPanelTests.swift:627:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureParentTaskPanelTests.swift:659:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureParentTaskPanelTests.swift:663:15: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelPublishTests.swift:110:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelPublishTests.swift:114:15: warning: [AddLines] add 1 line break
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:594:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:971:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2272:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2301:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2407:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2528:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4120:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4152:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4185:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5536:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5577:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5617:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5794:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5845:45: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5912:46: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5945:45: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5988:45: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6052:45: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6140:45: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6168:45: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6215:45: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6260:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6296:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
/tmp/bob-mac-capture-go12.BHqRrC/Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6337:18: warning: [TrailingComma] remove trailing comma from the last element in single line collection literal
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:15:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:16:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:191:90: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:300:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:645:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:687:24: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:687:61: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:688:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:689:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:690:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:691:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:718:100: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:754:101: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:852:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:886:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:887:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:892:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:926:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:927:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:967:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1007:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1036:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1065:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1092:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1183:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1199:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1297:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1316:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1335:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1359:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1364:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1449:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1718:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1752:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1757:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:1778:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2048:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2076:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2353:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2449:101: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2547:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2718:91: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:2760:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3205:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3261:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3310:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3357:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3430:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3509:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3559:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3583:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3672:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3782:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3800:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3831:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3851:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3855:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:3881:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4174:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4192:25: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4203:23: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4313:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4340:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4363:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4398:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4422:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4524:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4548:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4552:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4666:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4694:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4735:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4736:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:4977:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5062:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5067:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5068:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5103:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5104:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5117:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5174:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5201:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5236:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5256:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5260:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5281:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5300:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5328:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5381:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5392:39: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5393:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5394:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5395:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5405:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5415:39: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5416:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5417:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5418:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5455:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5480:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5487:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5492:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5517:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5529:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5567:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5607:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5612:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5635:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5640:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5669:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5670:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5696:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5721:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5727:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5732:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5733:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5735:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5740:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5753:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5769:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5782:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5783:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5799:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5812:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5824:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5828:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5841:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5863:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5867:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5880:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5922:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5927:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5940:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5959:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5964:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5977:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5978:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:5999:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6005:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6018:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6031:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6044:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6075:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6088:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6096:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6099:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6104:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6112:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6141:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6145:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6172:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6178:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6183:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6212:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6231:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6282:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6303:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6421:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6477:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6503:101: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6510:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6536:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6571:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6583:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6599:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6614:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6629:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6654:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6693:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6760:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6766:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6776:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6806:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6848:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6900:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6908:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6964:24: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6964:79: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6965:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:6966:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7158:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7204:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7224:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7275:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7321:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7326:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7438:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7443:99: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7443:112: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7450:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7472:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7488:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7575:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7672:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7735:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7739:15: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7778:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/CapturePanelModelTests.swift:7779:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/CapturePanelAgendaLayoutTests.swift:32:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelAgendaLayoutTests.swift:36:15: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CapturePanelAgendaLayoutTests.swift:222:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelAgendaLayoutTests.swift:229:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelAgendaLayoutTests.swift:251:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/CapturePanelAgendaLayoutTests.swift:268:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/CapturePanelAgendaLayoutTests.swift:269:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CapturePanelAgendaLayoutTests.swift:269:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/CaptureListPanelTests.swift:341:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureListPanelTests.swift:571:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureListPanelTests.swift:582:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureInboxRouteChoiceModelTests.swift:298:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureInboxRouteChoiceDesignTests.swift:16:24: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureInboxRouteChoiceDesignTests.swift:16:47: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureInboxRouteChoiceDesignTests.swift:17:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureInboxRouteChoiceDesignTests.swift:40:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureInboxRouteChoiceDesignTests.swift:68:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureInboxRouteChoiceDesignTests.swift:69:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureInboxRouteChoiceDesignTests.swift:71:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureInboxRouteChoiceDesignTests.swift:86:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureInboxRouteChoiceDesignTests.swift:87:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureInboxRouteChoiceDesignTests.swift:103:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureFileUnderPanelTests.swift:182:15: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:23:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:23:35: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:24:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:25:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:26:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:27:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:28:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:105:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:142:36: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:142:45: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:143:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:144:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:145:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:146:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:147:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:183:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:183:35: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:184:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:185:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:189:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:189:35: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:190:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:191:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:191:14: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:231:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:231:35: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:232:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:233:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:237:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:237:35: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:238:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:239:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:315:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:315:35: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:316:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:317:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:342:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:342:35: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:343:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:344:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:371:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:371:35: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:372:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:373:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:435:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:493:34: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:493:43: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:494:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:495:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:496:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:497:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:498:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureEditorHighlightTests.swift:674:1: warning: [Indentation] unindent by 2 spaces
Tests/BobMacCaptureTests/CaptureDependencyPanelTests.swift:91:100: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureDependencyPanelTests.swift:91:121: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureDependencyPanelTests.swift:293:29: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureDependencyPanelTests.swift:293:32: warning: [RemoveLine] remove line break
Tests/BobMacCaptureTests/CaptureDependencyPanelTests.swift:307:29: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureDependencyPanelTests.swift:307:32: warning: [RemoveLine] remove line break
Tests/BobMacCaptureTests/CaptureDependencyPanelTests.swift:325:95: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureCloseTaskCommaTests.swift:288:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureCloseTaskCommaTests.swift:292:15: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:154:14: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:155:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:156:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:156:11: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:289:14: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:290:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:291:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:291:11: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:332:14: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:333:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:334:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:334:11: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:349:14: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:350:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:351:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:352:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:352:11: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:377:18: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:378:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:379:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:380:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureClipPreviewHostedTests.swift:380:15: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureAgendaStoreTests.swift:11:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureAgendaStoreTests.swift:15:15: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureAgendaModelTests.swift:16:26: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureAgendaModelTests.swift:20:15: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureAgendaHeightConsistencyTests.swift:140:24: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Tests/BobMacCaptureTests/CaptureAgendaHeightConsistencyTests.swift:146:24: warning: [UseLetInEveryBoundCaseVariable] move this 'let' keyword inside the 'case' pattern, before each of the bound variables
Tests/BobMacCaptureTests/CaptureAgendaHeightConsistencyTests.swift:188:24: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureAgendaDesignTests.swift:18:14: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureAgendaDesignTests.swift:19:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureAgendaDesignTests.swift:20:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/CaptureAgendaDesignTests.swift:20:30: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CaptureAgendaDesignTests.swift:223:28: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/CanceledDraftStashTests.swift:101:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BundleSigningInspectorTests.swift:43:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BundleSigningInspectorTests.swift:44:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4:1: warning: [OrderedImports] sort import statements lexicographically
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:53:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:54:29: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:57:27: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:127:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:131:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:135:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:139:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:153:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:157:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:161:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:298:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:312:39: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:313:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:314:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:315:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:316:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:317:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:335:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:350:27: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:355:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:434:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:499:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:500:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:501:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:514:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:515:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:516:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:529:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:538:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:547:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:548:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:549:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:557:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:571:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:573:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:577:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:585:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:597:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:601:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:605:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:609:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:610:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:611:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:613:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:617:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:657:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:658:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:663:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:683:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:684:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:696:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:701:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:702:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:703:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:711:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:747:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:748:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:769:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:780:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:785:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:794:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:803:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:804:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:809:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:814:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:820:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:844:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:848:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:867:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:868:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:869:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:887:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:888:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:911:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:912:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:921:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:922:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:933:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:939:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:945:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:958:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:963:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:964:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:965:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:973:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:985:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:990:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:991:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1001:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1004:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1005:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1040:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1044:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1073:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1078:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1091:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1092:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1093:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1115:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1124:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1128:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1145:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1149:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1153:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1232:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1236:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1240:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1244:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1252:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1254:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1258:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1262:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1265:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1268:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1271:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1277:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1279:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1296:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1298:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1302:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1305:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1307:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1310:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1313:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1316:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1487:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1491:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1495:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1503:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1504:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1505:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1506:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1511:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1512:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1513:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1514:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1567:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1568:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1575:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1583:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1584:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1586:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1707:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1719:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1722:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1749:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1765:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1766:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1769:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:1770:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2247:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2297:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2406:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2413:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2450:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2451:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2452:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2453:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2454:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2479:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2493:99: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2493:106: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2504:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2505:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2506:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2507:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2508:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2509:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2510:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2511:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2512:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2513:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2514:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2515:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2516:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2517:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2518:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2519:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2520:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2521:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2522:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2523:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2524:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2525:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2526:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2527:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2528:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2529:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2530:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2531:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2532:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2533:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2534:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2535:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2536:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2537:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2538:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2539:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2540:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2541:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2542:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2543:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2544:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2545:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2546:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2547:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2548:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2549:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2550:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2551:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2552:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2553:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2554:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2555:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2556:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2557:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2558:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2559:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2560:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2561:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2562:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2563:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2564:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2565:1: warning: [Indentation] indent by 8 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2574:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2585:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2600:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2607:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2636:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2643:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2666:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2673:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2680:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2687:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2694:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2717:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2725:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2763:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2790:101: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2790:108: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2796:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2800:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2803:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2811:18: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2812:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2813:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2814:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2814:14: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2837:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2893:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:2898:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3368:25: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3369:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3370:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3371:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3372:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3372:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3373:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3373:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3374:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3375:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3375:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3376:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3376:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3377:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3378:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3378:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3379:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3395:27: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3396:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3397:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3398:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3399:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3399:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3400:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3400:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3401:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3401:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3402:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3402:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3403:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3404:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3405:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3422:19: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3423:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3423:84: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3424:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3425:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3426:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3427:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3428:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3428:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3429:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3430:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3430:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3431:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3431:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3432:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3432:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3433:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3434:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3435:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3436:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3437:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3437:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3438:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3439:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3440:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3441:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3442:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3443:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3444:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3445:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3446:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3447:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3448:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3449:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3450:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3451:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3452:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3453:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3454:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3455:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3456:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3457:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3458:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3813:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3816:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3835:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3839:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3871:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3874:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3889:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3907:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3925:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3941:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3951:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3960:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3971:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3982:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:3993:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4007:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4011:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4015:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4019:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4023:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4027:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4042:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4057:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4072:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4087:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4103:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4119:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4643:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4647:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4763:14: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4764:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4765:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4766:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4766:10: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4778:14: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4779:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4780:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4781:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BobMacCaptureTests.swift:4781:10: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BlockIDFieldFocusTests.swift:40:35: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/BlockIDFieldFocusTests.swift:41:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BlockIDFieldFocusTests.swift:42:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BlockIDFieldFocusTests.swift:43:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BlockIDFieldFocusTests.swift:44:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BlockIDFieldFocusTests.swift:45:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/BlockIDFieldFocusTests.swift:133:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/BlockIDFieldFocusTests.swift:137:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/AppRelauncherTests.swift:91:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:63:23: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:64:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:65:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:66:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:66:14: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:82:1: warning: [LineLength] line is too long
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:89:23: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:90:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:91:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:92:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:92:14: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:103:20: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:104:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:105:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:124:23: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:125:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:126:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:127:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:127:14: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:153:23: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:154:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:155:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:156:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:156:14: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:188:20: warning: [AddLines] add 1 line break
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:189:1: warning: [Indentation] indent by 4 spaces
Tests/BobMacCaptureTests/AXHighlightsTabsReaderTests.swift:190:1: warning: [Indentation] indent by 4 spaces
swift build --build-tests
/home/bryan/.local/share/funky/funky.sh: line 29: XDG_DATA_HOME: unbound variable
Building for debugging...
[0/21] Write sources
[5/21] Write swift-version--413BBEA0737331CC.txt
[7/111] Compiling CaptureCore CapturePickerPresentation.swift
[8/111] Compiling CaptureCore CapturePlanBudgetPresentation.swift
[9/112] Compiling CaptureCore CaptureEditWrite.swift
[10/112] Compiling CaptureCore CaptureGrammarGate.swift
[11/112] Compiling CaptureCore CaptureCompletionMenu.swift
[12/112] Compiling CaptureCore CaptureDrawerMenuPresentation.swift
[13/112] Compiling CaptureCore ActiveTaskPickerPresentation.swift
/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[14/112] Compiling CaptureCore BlockIDPickerIndex.swift
/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[15/112] Compiling CaptureCore CaptureAgendaInlineText.swift
/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[16/112] Compiling CaptureCore CaptureAgendaLayout.swift
/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureAgendaLayout.swift:312:13: warning: variable 'calendar' was never mutated; consider changing to 'let' constant
310 |             return nil
311 |         }
312 |         var calendar = calendar
    |             `- warning: variable 'calendar' was never mutated; consider changing to 'let' constant
313 |         let components = DateComponents(
314 |             year: year,
[17/112] Compiling CaptureCore BobMacCaptureLaunchContext.swift
[18/112] Compiling CaptureCore BobProcessClient.swift
[19/112] Compiling CaptureCore CaptureAgendaFitPlanner.swift
[20/112] Compiling CaptureCore CaptureAgendaHold.swift
[21/112] Compiling CaptureCore BlockIDRules.swift
[22/112] Compiling CaptureCore BobEnvironment.swift
[23/112] Compiling CaptureCore BobErrors.swift
[24/112] Compiling CaptureCore BobExecutableResolver.swift
[25/112] Compiling CaptureCore CanceledDraftStashStore.swift
[26/112] Compiling CaptureCore CaptureAgendaBoundaryRefresh.swift
[27/112] Compiling CaptureCore CapturePomodoroClosePresentation.swift
[28/112] Compiling CaptureCore CapturePomodoroLineTokens.swift
[29/112] Compiling CaptureCore CaptureRelationshipPresentation.swift
[30/112] Compiling CaptureCore CaptureRelationCloseEffect.swift
[31/112] Compiling CaptureCore CapturePomodoroResetPresentation.swift
[32/112] Compiling CaptureCore CapturePomodoroShiftPresentation.swift
[33/112] Compiling CaptureCore CaptureTogglePresentation.swift
[34/112] Compiling CaptureCore CaptureRefPresentation.swift
[35/112] Compiling CaptureCore DependencyPickerPresentation.swift
/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[36/112] Compiling CaptureCore CaptureSuccessorOfferRows.swift
[37/112] Emitting module CaptureCore
/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
343 | /// name 70%, route 60%, section 40%.
344 | private struct ActiveTaskPickerIndexEntry: Sendable {
345 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
346 |     let bobIndex: Int
347 |     let display: TaskDisplayText

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 951 | /// section 40%, status name 30%.
 952 | private struct BlockIDLinkEntry: Sendable {
 953 |     let candidate: CaptureCompletionCandidate
     |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
 954 |     let bobIndex: Int
 955 |     let display: TaskDisplayText

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/DependencyPickerPresentation.swift:569:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
567 | /// locator stays searchable.
568 | private struct DependencyPickerIndexEntry: Sendable {
569 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'DependencyPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
570 |     let bobIndex: Int
571 |     let display: TaskDisplayText

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[38/112] Compiling CaptureCore WorkBadgeTone.swift
[39/112] Compiling CaptureCore FuzzyMatcher.swift
[40/112] Compiling CaptureCore ObsidianOpenURL.swift
[41/112] Compiling CaptureCore CaptureSuccessorPresentation.swift
[42/112] Compiling CaptureCore CaptureRelationHeldPresentation.swift
[43/112] Compiling CaptureCore CaptureRelationSuccessorModels.swift
[44/112] Compiling CaptureCore ParentTaskPickerPresentation.swift
/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/ParentTaskPickerPresentation.swift:594:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
592 | 
593 | private struct ParentTaskPickerIndexEntry: Sendable {
594 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ParentTaskPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
595 |     let bobIndex: Int
596 |     let display: TaskDisplayText

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[45/112] Compiling CaptureCore CaptureRelationshipCopy.swift
[46/112] Compiling CaptureCore CapturePomodoroLinkPresentation.swift
[47/112] Compiling CaptureCore CapturePomodoroMergePresentation.swift
[48/112] Compiling CaptureCore CaptureRelationCancelPresentation.swift
[49/112] Compiling CaptureCore PomodoroHomes.swift
[50/112] Compiling CaptureCore CaptureTaskBlockPresentation.swift
[51/112] Compiling CaptureCore ProjectTaskMovePickerPresentation.swift
/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/ProjectTaskMovePickerPresentation.swift:280:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
278 | 
279 | private struct ProjectTaskMovePickerIndexEntry: Sendable {
280 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ProjectTaskMovePickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
281 |     let bobIndex: Int
282 |     let display: TaskDisplayText

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[52/112] Compiling CaptureCore CaptureTaskThemePresentation.swift
[53/112] Compiling CaptureCore CaptureRelatedModels.swift
[54/112] Compiling CaptureCore CaptureTargetsCache.swift
[55/112] Compiling CaptureCore CaptureTaskTypeMenuPresentation.swift
[56/112] Compiling CaptureCore CaptureUnconfiguredThemePresentation.swift
[57/112] Compiling CaptureCore CapturePomodoroSplitPresentation.swift
[58/112] Compiling CaptureCore CapturePomodoroStartPresentation.swift
[59/112] Compiling CaptureCore CaptureTodayPomodoroGoto.swift
[60/112] Compiling CaptureCore CaptureRelationCompletePresentation.swift
[61/112] Compiling CaptureCore CaptureTextRanges.swift
[62/112] Compiling CaptureCore CaptureProjectNotePresentation.swift
[63/112] Compiling CaptureCore CaptureRefFileUnder.swift
[64/112] Compiling CaptureCore CompletionRowContent.swift
[65/112] Compiling CaptureCore CaptureSavedTemplates.swift
[66/112] Compiling CaptureCore CapturePomodoroAdjustPresentation.swift
[67/112] Compiling CaptureCore CapturePomodoroBlockPresentation.swift
[68/112] Compiling CaptureCore CaptureTaskCompletePresentation.swift
[69/112] Compiling CaptureCore CaptureTransferPresentation.swift
/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureTransferPresentation.swift:311:35: error: constant 'self.rows' captured by a closure before being initialized
309 |         let noun = count == 1 ? "task" : "tasks"
310 |         headerText = "⤵ Merges \(count) \(noun) into \(targetLabel)"
311 |         rows = capture.merges.map { merge in
    |                                   `- error: constant 'self.rows' captured by a closure before being initialized
312 |             let text = merge.message.isEmpty
313 |                 ? "\(merge.source.title ?? merge.source.blockID ?? "Task") → \(targetLabel)"
[70/112] Compiling CaptureCore CaptureSubBulletPresentation.swift
[71/112] Compiling CaptureCore TaskLinkPickerPresentation.swift
/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/TaskLinkPickerPresentation.swift:493:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
491 | /// searchable.
492 | private struct TaskLinkPickerIndexEntry: Sendable {
493 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskLinkPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
494 |     let bobIndex: Int
495 |     let display: TaskDisplayText

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[72/112] Compiling CaptureCore SimilarTasksBandEdits.swift
[73/112] Compiling CaptureCore SimilarTasksBandPresentation.swift
[74/112] Compiling CaptureCore WikilinkTaskPickerPresentation.swift
/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/WikilinkTaskPickerPresentation.swift:472:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
470 | /// locator stays searchable.
471 | struct WikilinkTaskPickerIndexEntry: Sendable {
472 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'WikilinkTaskPickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
473 |     let bobIndex: Int
474 |     let display: TaskDisplayText

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[75/112] Compiling CaptureCore TaskDisplayText.swift
[76/112] Compiling CaptureCore SimilarTasksBandPolicy.swift
[77/112] Compiling CaptureCore CaptureOpenHintPresentation.swift
[78/112] Compiling CaptureCore CaptureOpenPlan.swift
[79/112] Compiling CaptureCore CapturePanelPlacement.swift
[80/112] Compiling CaptureCore CapturePickerHelpers.swift
[81/112] Compiling CaptureCore TaskCompletePickerPresentation.swift
/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/TaskCompletePickerPresentation.swift:534:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
532 | /// suggestion, so the locator stays searchable.
533 | struct TaskCompletePickerIndexEntry: Sendable {
534 |     let candidate: CaptureCompletionCandidate
    |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'TaskCompletePickerIndexEntry' has non-sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
535 |     let bobIndex: Int
536 |     let display: TaskDisplayText

/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:9059:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9057 | }
 9058 | 
 9059 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
      |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
 9060 |     public let replacement: String
 9061 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,
[82/112] Compiling CaptureCore CaptureCloseTaskCommaAssist.swift
[83/112] Compiling CaptureCore CaptureCloseTaskCommaProvenance.swift
[84/112] Compiling CaptureCore CaptureAgendaRefreshFilter.swift
[85/112] Compiling CaptureCore CaptureAgendaRefreshState.swift
[86/112] Compiling CaptureCore CaptureAgendaModels.swift
[87/112] Compiling CaptureCore CaptureAgendaPresentation.swift
[88/112] Compiling CaptureCore CaptureBlockIDSplice.swift
[89/112] Compiling CaptureCore CaptureClipPresentation.swift
[90/112] Compiling CaptureCore CaptureAgendaVisibility.swift
[91/112] Compiling CaptureCore CaptureBlockDiffRow.swift
[92/112] Compiling CaptureCore CaptureLinkGuardPresentation.swift
[93/112] Compiling CaptureCore CaptureList.swift
[94/112] Compiling CaptureCore CaptureModels.swift
/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:8858:13: warning: no calls to throwing functions occur within 'try' expression
 8856 |         let container = try decoder.singleValueContainer()
 8857 |         // Explicit null has no value; treat it as absent.
 8858 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8859 |             throw DecodingError.valueNotFound(
 8860 |                 CaptureThemeSuggestion.self,
[95/112] Compiling CaptureCore CaptureNotePullPresentation.swift
/tmp/bob-mac-capture-go12.BHqRrC/Sources/CaptureCore/CaptureModels.swift:8858:13: warning: no calls to throwing functions occur within 'try' expression
 8856 |         let container = try decoder.singleValueContainer()
 8857 |         // Explicit null has no value; treat it as absent.
 8858 |         if (try? container.decodeNil()) == true {
      |             `- warning: no calls to throwing functions occur within 'try' expression
 8859 |             throw DecodingError.valueNotFound(
 8860 |                 CaptureThemeSuggestion.self,
[96/112] Compiling CaptureCore CaptureInboxRoutePresentation.swift
[97/112] Compiling CaptureCore CaptureLineCaseToggle.swift
error: recipe `portable-check` failed on line 26 with exit code 1
Mac: setup=0 copy=0 bundle=1 typecheck-tests=1
Athena: setup=0 copy=0 portable-check=1
failed  exit=1  duration=143547ms

