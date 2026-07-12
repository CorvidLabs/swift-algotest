---
spec: algotest.spec.md
---

## Requirements

- **REQ-swift-algotest-001** (stable): Sandbox, account, and pool utilities shall preserve their existing asynchronous lifecycle, isolation, funding, and release behavior.
- **REQ-swift-algotest-002** (stable): Transaction builders, scenarios, mocks, and assertions shall provide deterministic Algorand test behavior without hidden live-network access.
- **REQ-swift-algotest-003** (stable): Snapshot capture and storage shall preserve the existing before/after state and comparison semantics across concurrent tests.
- **REQ-swift-algotest-004** (stable): Native verification shall build and test the package without implicitly starting a sandbox or requiring live credentials.

## Constraints

- Supported platform minimums and Swift 6 package compatibility remain as declared in `Package.swift`.
- Live sandbox behavior requires explicitly configured external services.

## Out of Scope

- Changing public testing APIs, dependency versions, platform minimums, releases, or live network configuration.
