---
change: CHG-0005-freeze-swiftpm-dependency-resolution-in-the-algotest-verification-lane
artifact: testing
---

# Testing

- Compare `Package.resolved` with main before and after verification.
- Run `fledge lanes run verify`; both tasks must use `--disable-automatic-resolution`.
- Confirm Swift builds and all 83 tests pass.
- Run strict SpecSync at 100% coverage and lifecycle enforcement.
- Confirm no files under `Sources/` or `Tests/` changed.
