---
change: CHG-0001-adopt-specsync-5-0-1-and-trust-1-0-0-governance-for-swift-algotest
artifact: requirements
---

# Requirements

## REQ-algotest-001

Sandbox, account, and pool utilities SHALL preserve their existing asynchronous lifecycle, isolation, funding, and release behavior.

## REQ-algotest-002

Transaction builders, scenarios, mocks, and assertions SHALL provide deterministic Algorand test behavior without hidden live-network access.

## REQ-algotest-003

Snapshot capture and storage SHALL preserve the existing before/after state and comparison semantics across concurrent tests.

## REQ-algotest-004

Native verification SHALL build and test the package without implicitly starting a sandbox or requiring live credentials.
