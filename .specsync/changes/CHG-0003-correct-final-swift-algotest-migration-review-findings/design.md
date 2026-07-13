---
change: CHG-0003-correct-final-swift-algotest-migration-review-findings
artifact: design
---

# Design

Restore the lockfile byte-for-byte from main so the migration cannot alter dependency resolution. Make canonical specs, agent integration directories, README, and existing governance files meaningful without an ignored-path override. Use Gemini's documented `{{args}}` substitution and classify complete create-spec input after removing `--minimal`, accepting it as a module name only when it is one whitespace-free identifier.
