---
spec: algotest.spec.md
---

## Requirements

## Constraints

- Supported platform minimums and Swift 6 package compatibility remain as declared in `Package.swift`.
- Live sandbox behavior requires explicitly configured external services.

## Out of Scope

- Changing public testing APIs, dependency versions, platform minimums, releases, or live network configuration.

### REQ-algotest-001

AlgoTest account, pool, and sandbox utilities SHALL preserve their existing asynchronous lifecycle, isolation, funding, and release behavior.

Acceptance Criteria

- Existing account, pool, and sandbox lifecycle tests pass without live credentials.

### REQ-algotest-002

AlgoTest transaction builders, scenarios, mocks, and assertions SHALL provide deterministic behavior without hidden live-network access.

Acceptance Criteria

- Existing transaction, mock, assertion, and deterministic integration tests pass without contacting a live network.

### REQ-algotest-003

AlgoTest snapshot capture and storage SHALL preserve existing before-and-after state and comparison semantics.

Acceptance Criteria

- Existing snapshot capture, storage, and comparison tests pass.

### REQ-algotest-004

Native verification SHALL build and test AlgoTest without implicitly starting sandbox infrastructure or requiring live credentials.

Acceptance Criteria

- The Fledge verification lane completes Swift build and all deterministic tests without live credentials.
