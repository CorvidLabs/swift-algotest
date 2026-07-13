---
change: CHG-0005-freeze-swiftpm-dependency-resolution-in-the-algotest-verification-lane
artifact: context
---

# Context

`Package.resolved` on main omits two direct pins that SwiftPM can infer from already-recorded transitive resolution. Ordinary `swift build` rewrites the lockfile even though dependency constraints are unchanged. Both build and all 83 tests pass with `--disable-automatic-resolution`, which prevents verification from turning that local rewrite into an unintended migration diff.
