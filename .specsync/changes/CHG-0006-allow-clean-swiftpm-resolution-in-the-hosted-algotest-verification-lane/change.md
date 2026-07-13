---
id: CHG-0006-allow-clean-swiftpm-resolution-in-the-hosted-algotest-verification-lane
state: accepted
type: bug_fix
base_commit: 0546627ddbb42c2cc092362b6aa288d7fafd74be
---

# Allow clean SwiftPM resolution in the hosted AlgoTest verification lane

## Intent

Allow clean SwiftPM resolution in the hosted AlgoTest verification lane

## Affected Canonical Specs

- None

## Acceptance Criteria

- The Fledge verification lane permits SwiftPM to resolve the existing manifest constraints in a clean checkout and removes its ephemeral lockfile rewrite on exit; Swift builds and all 83 tests pass; Package.resolved remains byte-identical to main; no source or test files change

## No-spec Rationale

The base branch lockfile is incomplete for a clean checkout, so hosted verification must allow SwiftPM to resolve the existing manifest constraints while the migration continues to commit no dependency-lock change and alters no source, tests, APIs, or canonical requirements.
