---
change: CHG-0001-adopt-specsync-5-0-1-and-trust-1-0-0-governance-for-swift-algotest
artifact: testing
---

# Testing

- Strict SpecSync at advisory threshold zero
- All four agent integrations and Trust doctor
- `swift build`
- `swift test`: 83 passed, zero failures
- Existing macOS and Swift 6 Linux hosted workflows
- No live sandbox or network access

## Requirement Evidence

- `REQ-algotest-001`: account, sandbox, and pool lifecycle tests in `Tests/AlgoTestTests/AccountTests.swift` and `Tests/AlgoTestTests/SandboxTests.swift`.
- `REQ-algotest-002`: transaction, mocking, assertion, and integration tests in `Tests/AlgoTestTests/TransactionTests.swift`, `MockingTests.swift`, `AssertionTests.swift`, and `IntegrationTests.swift`.
- `REQ-algotest-003`: snapshot behavior tests in `Tests/AlgoTestTests/SnapshotTests.swift`.
- `REQ-algotest-004`: the Fledge `verify` lane runs `swift build` and `swift test` without live credentials or sandbox startup.
