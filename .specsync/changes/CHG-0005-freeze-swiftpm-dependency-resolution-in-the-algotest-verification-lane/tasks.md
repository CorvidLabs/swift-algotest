---
change: CHG-0005-freeze-swiftpm-dependency-resolution-in-the-algotest-verification-lane
artifact: tasks
---

# Tasks

- [x] Restore `Package.resolved` byte-for-byte from main.
- [x] Confirm frozen SwiftPM build succeeds without changing the lockfile.
- [x] Confirm all 83 tests pass with frozen SwiftPM resolution.
- [x] Configure the Fledge verification lane to use frozen resolution.
- [x] Prepare strict SpecSync validation with no source or test changes.
