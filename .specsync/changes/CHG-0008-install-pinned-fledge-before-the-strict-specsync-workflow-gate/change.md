---
id: CHG-0008-install-pinned-fledge-before-the-strict-specsync-workflow-gate
state: accepted
type: bug_fix
base_commit: 824c01da7c3115a948613c3983dfef6f491ca254
---

# Install pinned Fledge before the strict SpecSync workflow gate

## Intent

Install pinned Fledge before the strict SpecSync workflow gate

## Affected Canonical Specs

- None

## Acceptance Criteria

- The hosted workflow installs Fledge 1.7.0 from its immutable release asset and verifies the approved SHA-256 before the strict SpecSync action; strict 100 percent SpecSync and lifecycle enforcement can execute the native lane before Trust; local native build and all 83 tests pass; no product or lockfile changes are committed

## No-spec Rationale

The strict SpecSync action executes the configured native Fledge verification lane, so the hosted runner must install the same pinned and checksum-verified Fledge runtime before that action; this changes no product source, tests, APIs, or canonical requirements.
