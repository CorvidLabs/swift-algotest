---
change: CHG-0002-correct-swift-algotest-governance-coverage-and-canonical-requirement-traceabilit
artifact: testing
---

# Testing

- `REQ-algotest-001`: `AccountTests.swift` and `SandboxTests.swift`.
- `REQ-algotest-002`: `TransactionTests.swift`, `MockingTests.swift`, `AssertionTests.swift`, and `IntegrationTests.swift`.
- `REQ-algotest-003`: `SnapshotTests.swift`.
- `REQ-algotest-004`: the Fledge `verify` lane runs `swift build` and `swift test` without live credentials.
- Strict SpecSync must report 100% file and LOC coverage with no warnings.
