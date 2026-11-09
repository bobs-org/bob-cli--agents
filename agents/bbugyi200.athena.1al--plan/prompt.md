#gh:gh_bobs-org__bob-cli The bob-mac-capture app's `just install` command is failing (see the partial
command output below for context). Can you help me diagnose the root cause of this
issue, fix it, and leave appropriate notes on the epic bead that introduced it (if any)?
#plan %m:@xlarge

```
  ✗ build failed after 1:55 · exit 1
      /Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/ActiveTaskPickerPresentation.swift:345:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
      343 | /// name 70%, route 60%, section 40%.
      344 | private struct ActiveTaskPickerIndexEntry: Sendable {
      345 |     let candidate: CaptureCompletionCandidate
          |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'ActiveTaskPickerIndexEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
      346 |     let bobIndex: Int
      347 |     let display: TaskDisplayText

      /Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/CaptureModels.swift:10399:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
      10397 | }
      10398 |
      10399 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
            |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
      10400 |     public let replacement: String
      10401 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

      /Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/BlockIDPickerIndex.swift:953:9: warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
       951 | /// section 40%, status name 30%.
       952 | private struct BlockIDLinkEntry: Sendable {
       953 |     let candidate: CaptureCompletionCandidate
           |         `- warning: stored property 'candidate' of 'Sendable'-conforming struct 'BlockIDLinkEntry' has non-Sendable type 'CaptureCompletionCandidate'; this is an error in the Swift 6 language mode
       954 |     let bobIndex: Int
       955 |     let display: TaskDisplayText

      /Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/CaptureModels.swift:10399:15: note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
      10397 | }
      10398 |
      10399 | public struct CaptureCompletionCandidate: Codable, Equatable, Identifiable {
            |               `- note: consider making struct 'CaptureCompletionCandidate' conform to the 'Sendable' protocol
      10400 |     public let replacement: String
      10401 |     /// Additive `directive` row fields: the literal `%` token, a one-line `summary`,

      /Users/bbugyi/projects/github/bobs-org/bob-mac-capture/Sources/CaptureCore/BobExecutableResolver.swift:4:16: warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
       2 |
       3 | public struct BobExecutableResolver: Sendable {
       4 |     public let fileManager: FileManager
         |                `- warning: stored property 'fileManager' of 'Sendable'-conforming struct 'BobExecutableResolver' has non-Sendable type 'FileManager'; this is an error in the Swift 6 language mode
       5 |     public let homeDirectory: URL
       6 |     public let candidates: [String]

      full log  ~/.local/state/bob-cli/install-all/logs/20261109-135435-7872-bob-mac-capture.log
      rerun with  just install-all -v  to stream build output
  ✗ 2 new commits · 2f1d6dd → ef5dc4a · install failed (exit 1)

🔄  OBSIDIAN
────────────────────────────────────────────────
  – plugins unchanged · restart not needed

✨  SUMMARY
────────────────────────────────────────────────
  ✓  bob-cli          4 new commits · 3c1b6451 → 0a74731b · installed @ 0a74731b  3m 52s
  ✓  bob-plugins      up to date · a2045cc · 9/9 plugins in sync  5s
  ✗  bob-mac-capture  2 new commits · 2f1d6dd → ef5dc4a · install failed (exit 1)  1m 57s
  –  obsidian         plugins unchanged · restart not needed

  ✗  1 STEP FAILED · 6m 01s · about usual (5–7 min)
  what's new  bob-cli 4 · feat(notebooks): recognize notebooks with l…, +3 more
  what's new  bob-mac-capture 2 · feat(capture): support modifier ali…, +1 more
error: recipe `install-all` failed on line 170 with exit code 1
```