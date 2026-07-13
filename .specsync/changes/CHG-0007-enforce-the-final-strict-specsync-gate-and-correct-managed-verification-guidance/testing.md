---
change: CHG-0007-enforce-the-final-strict-specsync-gate-and-correct-managed-verification-guidance
artifact: testing
---

# Testing

- Run released SpecSync 5.0.1 with strict checks, 100% coverage, and lifecycle enforcement.
- Confirm the workflow pins SpecSync and Trust to their approved immutable release commits.
- Run `fledge lanes run verify`; Swift must build and all 83 tests must pass.
- Confirm all four agent integrations remain installed and Fledge configuration validates strictly.
- Confirm `Package.resolved`, `Sources/`, and `Tests/` remain unchanged from `main`.
