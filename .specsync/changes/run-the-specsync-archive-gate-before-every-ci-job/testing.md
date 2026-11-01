---
change: run-the-specsync-archive-gate-before-every-ci-job
artifact: testing
---

# Testing

- Each edited workflow parses with Ruby Psych `safe_load`, and the job graph was
  printed: `archive-gate` has no needs; `build`, `macOS`, `trust` and `ubuntu`
  need `archive-gate`; `deploy` needs `build`.
- `bash .github/scripts/archive-readiness.sh .` from spec-sync at the pinned
  commit fails as designed, listing the open changes, which shows the gate
  blocks while changes are open.
- `specsync change audit --strict` and `specsync check --strict` (6.0.0, the
  version CI pins) were run; results are recorded in the pull request.
- In CI, the Archive job runs first and every other job is skipped until it
  passes.
