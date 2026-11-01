---
change: run-the-specsync-archive-gate-before-every-ci-job
artifact: plan
---

# Plan

## Approach

Add one `archive-gate` job (display name `Archive`) at the top of `jobs:` in each
workflow that runs on `pull_request` or `push`, and make every other job depend on
it, so nothing else runs while a SpecSync change is open.

## Out of scope

- Archiving, reopening or otherwise touching the preexisting changes CHG-0001 to
  CHG-0008.
- Changing the existing SpecSync lifecycle gate pin (`@v6`, version 6.0.0) or the
  Trust, Fledge and Swift build steps.
- Configuring the org ruleset that requires the `Archive` check.

## Steps

1. In `docs.yml`, `macOS.yml`, `trust.yml` and `ubuntu.yml`, add the
   `archive-gate` job on `ubuntu-latest` with a 5 minute timeout: check out the
   pull request head (`github.event.pull_request.head.sha || github.sha`) with
   `actions/checkout@v5` and `persist-credentials: false`, then run
   `CorvidLabs/spec-sync@106aaa43d0bcf049f19b173ddb63815a25c3f931` with
   `archive-gate-only: 'true'`.
2. Add `needs: archive-gate` to every job without `needs` (`build`, `macOS`,
   `trust`, `ubuntu`); `deploy` already needs `build` and reaches the gate
   transitively.
3. Leave every other line unchanged.

## Risks

- The Archive check stays red on every pull request until the preexisting
  accepted changes are archived by their owners.
- The commit pin must move to the first spec-sync release that ships the gate.

## Constraints consulted

- AGENTS.md (CorvidLabs trust toolchain block): the trust gate is kept in place
  and not weakened; the managed block and generated trust configuration are
  untouched; module specs are unaffected because no source changes.
