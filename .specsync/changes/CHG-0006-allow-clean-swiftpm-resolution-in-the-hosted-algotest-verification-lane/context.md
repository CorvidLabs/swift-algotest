---
change: CHG-0006-allow-clean-swiftpm-resolution-in-the-hosted-algotest-verification-lane
artifact: context
---

# Context

The base branch's committed `Package.resolved` does not contain the direct `swift-algokit` pin required by
`Package.swift`. A warm local SwiftPM cache can build with automatic resolution disabled, but a clean hosted
checkout rejects the same lockfile as out of date before compilation. This correction supersedes CHG-0005: the
verification lane permits SwiftPM to resolve existing manifest constraints, then restores its lock rewrite on exit.
