---
change: CHG-0008-install-pinned-fledge-before-the-strict-specsync-workflow-gate
artifact: testing
---

# Testing

- Confirm the workflow downloads Fledge 1.7.0 from its immutable release URL and rejects a checksum mismatch.
- Run released SpecSync 5.0.1 strict checks at 100% coverage and lifecycle enforcement.
- Run `fledge lanes run verify`; Swift must build and all 83 tests must pass.
- Confirm the workflow still pins SpecSync 5.0.1 and Trust 1.0.0 to approved immutable commits.
- Confirm `Package.resolved`, `Sources/`, and `Tests/` remain unchanged from `main`.
