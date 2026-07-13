---
spec: algotest.spec.md
---

## Context

AlgoTest is a pre-1.0 dependency for deterministic Swift Algorand testing. It combines protocol-oriented sandbox abstractions, concurrency-safe fixtures and mocks, transaction helpers, snapshots, and assertion utilities with macOS/Linux CI and DocC Pages.

## Related Modules

- `swift-algorand` supplies protocol types and clients.
- `swift-algokit` supplies local sandbox integration.

## Design Decisions

- Preserve mock-first deterministic verification.
- Keep sandbox startup and live network access explicit.
- Keep standalone DocC Pages publication outside Trust-managed Atlas.
