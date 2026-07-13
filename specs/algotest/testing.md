---
spec: algotest.spec.md
---

## Test Plan

- Run the existing account, assertion, error, mock, sandbox, snapshot, transaction, and deterministic integration tests.

- Build and test on the existing macOS and Swift 6 Linux workflows.
- Keep DocC Pages publication independent.
- Do not implicitly start local sandbox infrastructure or access live networks in Trust.

## Requirement Coverage

- `REQ-algotest-001`: account, sandbox, and pool lifecycle tests.
- `REQ-algotest-002`: transaction, mocking, assertion, and deterministic integration tests.
- `REQ-algotest-003`: snapshot capture, storage, and comparison tests.
- `REQ-algotest-004`: the native Fledge build-and-test verification lane.
