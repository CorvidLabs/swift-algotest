## ADDED

### REQUIREMENT REQ-algotest-001

Sandbox, account, and pool utilities SHALL preserve their existing asynchronous lifecycle, isolation, funding, and release behavior.

Acceptance Criteria

- Existing account, pool, and sandbox lifecycle tests pass without live credentials.

### REQUIREMENT REQ-algotest-002

Transaction builders, scenarios, mocks, and assertions SHALL provide deterministic Algorand test behavior without hidden live-network access.

Acceptance Criteria

- Existing transaction, mock, assertion, and deterministic integration tests pass without contacting a live network.

### REQUIREMENT REQ-algotest-003

Snapshot capture and storage SHALL preserve the existing before/after state and comparison semantics across concurrent tests.

Acceptance Criteria

- Existing snapshot capture, storage, and comparison tests pass under the package test lane.

### REQUIREMENT REQ-algotest-004

Native verification SHALL build and test the package without implicitly starting a sandbox or requiring live credentials.

Acceptance Criteria

- The Fledge verification lane completes Swift build and test commands without starting sandbox infrastructure.
