---
change: CHG-0006-allow-clean-swiftpm-resolution-in-the-hosted-algotest-verification-lane
artifact: tasks
---

# Tasks

- [x] Capture the clean hosted checkout failure caused by disabled automatic resolution.
- [x] Permit ordinary SwiftPM resolution in the Fledge build and test tasks.
- [x] Restore the ephemeral lockfile rewrite when each Fledge task exits.
- [x] Run the native Swift build and all 83 tests through the corrected Fledge lane.
- [x] Prepare strict SpecSync validation at 100% coverage with no source or test changes.
