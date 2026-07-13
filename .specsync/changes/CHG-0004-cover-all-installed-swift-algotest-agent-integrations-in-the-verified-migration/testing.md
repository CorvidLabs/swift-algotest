---
change: CHG-0004-cover-all-installed-swift-algotest-agent-integrations-in-the-verified-migration
artifact: testing
---

# Testing

- Run released SpecSync 5.0.1 strict validation at 100% coverage and lifecycle enforcement.
- Confirm Claude, Codex, Cursor, and Gemini report installed.
- Run the Fledge verification lane, Swift build, and all 83 tests.
- Confirm `Package.resolved` remains byte-identical to main.
- Confirm no files under `Sources/` or `Tests/` changed.
