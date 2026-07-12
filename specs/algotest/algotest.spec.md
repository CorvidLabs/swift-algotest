---
module: algotest
version: 1
status: active
files:
  - Package.swift

db_tables: []
depends_on: []
---

# Swift AlgoTest Utilities

## Purpose

Provide the existing Swift testing utilities for Algorand sandbox lifecycle, funded accounts, transaction scenarios, actor-based mock clients, state snapshots, and XCTest assertions across supported platforms.

## Public API

### Package Interface

The `AlgoTest` library product exposes sandbox protocols and state, account factories and pools, funded-account fixtures, transaction builders and scenarios, mock Algod and Indexer actors, snapshot capture and storage, and Algorand-specific assertion helpers.

## Invariants

1. Stateful test utilities use the existing actor and `Sendable` boundaries so concurrent tests do not introduce shared-state races.
2. Account pools release borrowed accounts according to their documented lifecycle even when a test operation fails.
3. Mock clients and snapshots remain deterministic and do not silently perform live blockchain requests.
4. Sandbox operations surface unavailable, already-running, stopped, and command failures explicitly.
5. Live sandbox or network integration remains separately configured and is not implicitly started by the blocking Trust lane.

## Behavioral Examples

```
Given deterministic funded accounts and a mock Algod client
When a test submits a transaction and captures surrounding state
Then assertions and snapshots report the existing balance and transaction changes without a live network
```

## Error Cases

| Error | When | Behavior |
|-------|------|----------|
| Sandbox unavailable | A requested local sandbox cannot be reached or managed | Return the existing sandbox error |
| Insufficient balance | A scenario cannot fund or afford the requested operation | Return an explicit balance error |
| Missing mock data | A mock query has no configured response | Return the configured mock failure |
| Missing snapshot | A requested snapshot identifier is absent | Return an explicit snapshot error |

## Dependencies

- Swift 6.0 or newer
- `swift-algorand` and `swift-algokit`
- XCTest and Foundation
- Swift-DocC plugin for independent documentation publication

## Change Log

| Version | Date | Changes |
|---------|------|---------|
| 1 | 2026-07-12 | Initial spec |
