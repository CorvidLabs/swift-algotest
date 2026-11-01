---
id: run-the-specsync-archive-gate-before-every-ci-job
state: draft
type: operations
base_commit: 0e0ca6f3dd26d2067a50f527ff2a1ae1b822dcba
---

# Run the SpecSync archive gate before every CI job

## Intent

Run the SpecSync archive gate before every CI job

## Affected Canonical Specs

- None

## Acceptance Criteria

- Each workflow that runs on pull_request or push (docs.yml, macOS.yml, trust.yml, ubuntu.yml) starts with an archive-gate job named Archive that checks out the pull request head and runs CorvidLabs/spec-sync pinned to 106aaa43d0bcf049f19b173ddb63815a25c3f931 with archive-gate-only 'true'; every other job needs archive-gate directly or transitively, so no other CI job runs while any change under .specsync/changes/ is open.

## No-spec Rationale

CI workflow ordering only; no canonical spec owns .github/workflows
