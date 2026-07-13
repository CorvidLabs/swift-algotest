---
change: CHG-0003-correct-final-swift-algotest-migration-review-findings
artifact: testing
---

# Testing

- Confirm `git diff main -- Package.resolved` is empty and `316a620` is an ancestor of HEAD.
- Validate the SDD JSON and both Gemini TOML commands parse successfully.
- Confirm all create-spec prompts classify complete input before selecting a module name.
- Run strict SpecSync at 100% coverage and lifecycle enforcement.
- Run the Fledge verification lane, Swift build, and all 83 tests.
- Confirm no files under `Sources/` or `Tests/` changed.
