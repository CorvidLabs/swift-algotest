---
change: CHG-0006-allow-clean-swiftpm-resolution-in-the-hosted-algotest-verification-lane
artifact: testing
---

# Testing

- Run `fledge lanes run verify` with automatic SwiftPM resolution available; the build and all 83 tests must pass.
- Confirm task exit cleanup removes the ephemeral SwiftPM lockfile rewrite and `Package.resolved` remains
  byte-identical to `main` after the full lane.
- Run strict SpecSync validation at 100% file, LOC, and export coverage plus lifecycle enforcement.
- Confirm no files under `Sources/` or `Tests/` changed.
