---
change: run-the-specsync-archive-gate-before-every-ci-job
artifact: context
---

# Context

This is part of the org-wide rollout of CorvidLabs/spec-sync#832, approved by
0xLeif. That pull request (merged as 106aaa43d0bcf049f19b173ddb63815a25c3f931)
added an archive gate to the spec-sync GitHub Action: with
`archive-gate-only: 'true'` it runs only `.github/scripts/archive-readiness.sh`
(bash and python3, no binary download) and fails while any change under
`.specsync/changes/` is still open. The goal is that every SpecSync change is
archived before a pull request merges, and that CI runs nothing else until it is.

Constraints for a session picking this up:

- Published spec-sync v6.1.1 and older ignore `archive-gate-only`, so the step
  pins commit 106aaa43d0bcf049f19b173ddb63815a25c3f931 until a release ships the
  gate. The existing `SpecSync lifecycle gate` step in `trust.yml` keeps its
  `@v6` / `version: "6.0.0"` pin unchanged.
- Branch protection is an org ruleset requiring a check named `Archive`,
  configured separately; a skipped job counts as passing, so merge blocking
  relies on that ruleset.
- Eight changes (CHG-0001 to CHG-0008) are already open in the `accepted` state on
  `main`. They belong to other owners and are not modified here; until they are
  archived the new Archive check stays red on every pull request.
