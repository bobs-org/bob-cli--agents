#gh:gh_bobs-org__bob-cli #fork:00r It's still not working (see the command output below for context). Do I need to install something on my mac first? #if_not_plan 
```
❯ just test
./Scripts/xcode-swift.sh test
error: the selected developer directory is not a full Xcode installation: /Library/Developer/CommandLineTools
  Standalone Command Line Tools do not include XCTest and other Xcode-only frameworks.
  Select the full Xcode application:
    sudo xcode-select --switch /Applications/Xcode.app
  Or scope the fix to one shell without changing the system default:
    export DEVELOPER_DIR=/Applications/Xcode.app/Contents/Developer
error: recipe `test` failed on line 16 with exit code 69
```