---
id: CHG-0005-freeze-swiftpm-dependency-resolution-in-the-algotest-verification-lane
state: accepted
type: bug_fix
base_commit: c01dc46e440cff438a9f956d0fee7e4578f43cc3
---

# Freeze SwiftPM dependency resolution in the AlgoTest verification lane

## Intent

Freeze SwiftPM dependency resolution in the AlgoTest verification lane

## Affected Canonical Specs

- None

## Acceptance Criteria

- The Fledge build and test tasks use frozen SwiftPM resolution; Package.resolved remains byte-identical to main before and after verification; Swift builds and all 83 tests pass; no source or test files change

## No-spec Rationale

This correction prevents governance verification from rewriting the dependency lock; it preserves the dependencies already committed on main and does not change source, tests, APIs, or canonical requirements.
