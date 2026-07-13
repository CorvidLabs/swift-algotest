---
change: CHG-0008-install-pinned-fledge-before-the-strict-specsync-workflow-gate
artifact: context
---

# Context

The strict SpecSync action runs the repository's configured `fledge lanes run verify` command. On the hosted Swift
container, Fledge was unavailable until the later Trust action installed its private runtime, so SpecSync correctly
failed with `No such file or directory` before validating the contract. The workflow must make the approved Fledge
1.7.0 binary available first and verify its immutable release checksum.
