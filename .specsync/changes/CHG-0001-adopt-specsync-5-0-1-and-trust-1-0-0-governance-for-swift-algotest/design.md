---
change: CHG-0001-adopt-specsync-5-0-1-and-trust-1-0-0-governance-for-swift-algotest
artifact: design
---

# Design

Preserve all existing workflows and dependency declarations. Add a separate Linux Swift 6 job named `trust`, pinned to immutable Trust 1.0.0. Delegate build and test to Fledge. Use advisory coverage zero, blocking risk, progressive provenance, and disable Trust-managed Atlas because DocC Pages remains independent.
