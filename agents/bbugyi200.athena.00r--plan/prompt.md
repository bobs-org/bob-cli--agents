#gh:gh_bobs-org__bob-cli I'm unable to run the `just test` command for the bob-mac-capture repo (see the command output below for context). Can you help me diagnose the root cause of this issue and fix it? #plan 
```
❯ just test
swift test
[1/1] Planning build
Building for debugging...
/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Tests/CaptureCoreTests/BobEnvironmentTests.swift:1:8: error: no such module 'XCTest'
 1 | import XCTest
   |        `- error: no such module 'XCTest'
 2 |
 3 | @testable import CaptureCore
/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Tests/CaptureCoreTests/BobEnvironmentTests.swift:1:8: error: no such module 'XCTest'
 1 | import XCTest
   |        `- error: no such module 'XCTest'
 2 |
 3 | @testable import CaptureCore
error: emit-module command failed with exit code 1 (use -v to see invocation)
/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Tests/CaptureCoreTests/BobEnvironmentTests.swift:1:8: error: no such module 'XCTest'
 1 | import XCTest
   |        `- error: no such module 'XCTest'
 2 |
 3 | @testable import CaptureCore
/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Tests/CaptureCoreTests/BobEnvironmentTests.swift:1:8: error: no such module 'XCTest'
 1 | import XCTest
   |        `- error: no such module 'XCTest'
 2 |
 3 | @testable import CaptureCore
/Users/bbugyi/projects/github/bbugyi200/bob-mac-capture/Tests/CaptureCoreTests/BobEnvironmentTests.swift:1:8: error: no such module 'XCTest'
 1 | import XCTest
   |        `- error: no such module 'XCTest'
 2 |
 3 | @testable import CaptureCore
[6/23] Compiling CaptureCoreTests BobProcessClientTests.swift
error: fatalError
error: recipe `test` failed on line 16 with exit code 1
```