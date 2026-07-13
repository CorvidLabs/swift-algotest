---
spec: algotest.spec.md
---

## Requirements

- **REQ-algotest-001** (stable): Sandbox, account, and pool utilities SHALL preserve their existing asynchronous lifecycle, isolation, funding, and release behavior.
- **REQ-algotest-002** (stable): Transaction builders, scenarios, mocks, and assertions SHALL provide deterministic Algorand test behavior without hidden live-network access.
- **REQ-algotest-003** (stable): Snapshot capture and storage SHALL preserve the existing before/after state and comparison semantics across concurrent tests.
- **REQ-algotest-004** (stable): Native verification SHALL build and test the package without implicitly starting a sandbox or requiring live credentials.

## Constraints

- Supported platform minimums and Swift 6 package compatibility remain as declared in `Package.swift`.
- Live sandbox behavior requires explicitly configured external services.

## Out of Scope

- Changing public testing APIs, dependency versions, platform minimums, releases, or live network configuration.
