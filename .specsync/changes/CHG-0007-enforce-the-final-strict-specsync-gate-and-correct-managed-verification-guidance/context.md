---
change: CHG-0007-enforce-the-final-strict-specsync-gate-and-correct-managed-verification-guidance
artifact: context
---

# Context

The standard Trust profile preserves progressive provenance, but it does not make SpecSync warnings blocking. The
migration already establishes complete canonical coverage, so the workflow must run the immutable SpecSync 5.0.1
action in strict mode at 100% before Trust. The managed agent block also referenced a nonexistent Fledge Trust
subcommand instead of the repository's configured `verify` lane.
