---
module: algotest
version: 2
status: active
files:
  - Package.swift
  - Sources/AlgoTest/Accounts/AccountFactory.swift
  - Sources/AlgoTest/Accounts/AccountPool.swift
  - Sources/AlgoTest/Accounts/FundedAccount.swift
  - Sources/AlgoTest/AlgoTestError.swift
  - Sources/AlgoTest/Assertions/AlgorandAssertions.swift
  - Sources/AlgoTest/Assertions/AssetAssertions.swift
  - Sources/AlgoTest/Assertions/BalanceAssertions.swift
  - Sources/AlgoTest/Assertions/TransactionAssertions.swift
  - Sources/AlgoTest/Mocking/MockAlgodClient.swift
  - Sources/AlgoTest/Mocking/MockIndexerClient.swift
  - Sources/AlgoTest/Mocking/MockResponses.swift
  - Sources/AlgoTest/Sandbox/LocalSandbox.swift
  - Sources/AlgoTest/Sandbox/Sandbox.swift
  - Sources/AlgoTest/Sandbox/SandboxState.swift
  - Sources/AlgoTest/Snapshots/SnapshotCapture.swift
  - Sources/AlgoTest/Snapshots/SnapshotStore.swift
  - Sources/AlgoTest/Snapshots/StateSnapshot.swift
  - Sources/AlgoTest/Transactions/TestTransactionBuilder.swift
  - Sources/AlgoTest/Transactions/TransactionScenarios.swift

db_tables: []
depends_on: []
---

# Swift AlgoTest Utilities

## Purpose

Provide the existing Swift testing utilities for Algorand sandbox lifecycle, funded accounts, transaction scenarios, actor-based mock clients, state snapshots, and XCTest assertions across supported platforms.

## Public API

### Exported Functions

| Export | Description |
|--------|-------------|
| `AccountFactory` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `Configuration` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `defaultFundingAmount` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `minimumBalance` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `createAccount` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `createAccounts` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `fundAccount` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `accounts` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `reset` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `init` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `AccountPool` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `poolSize` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `accountFunding` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `initialize` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `acquire` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `release` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `withAccount` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `statistics` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `Statistics` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `available` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `inUse` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `total` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `FundedAccount` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `address` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `privateKey` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `initialBalance` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `metadata` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `Metadata` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `createdAt` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `purpose` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `tags` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `mock` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `tagged` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `AlgoTestError` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `errorDescription` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `sandboxNotRunning` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `sandboxAlreadyRunning` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `sandboxStartupFailed` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `sandboxShutdownFailed` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `accountCreationFailed` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `fundingFailed` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `insufficientBalance` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `transactionBuildFailed` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assertionFailed` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `snapshotCaptureFailed` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `snapshotComparisonFailed` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `mockConfigurationError` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `invalidState` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assertValidAddress` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assertValidTransaction` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assertThrowsError` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assertNoThrow` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assertValidAssetID` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assertAssetHolding` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assertAssetConfig` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assertSufficientBalance` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assertBalanceInRange` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assertBalanceEquals` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assertCanAffordTransaction` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assertTransactionParties` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assertTransactionAmount` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assertTransactionNote` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assertTransactionFeeInRange` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assertBatchSameSender` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `MockAlgodClient` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `register` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `advance` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `accountInfo` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `transaction` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `status` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `getCurrentRound` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `submitTransaction` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `registeredAccounts` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `MockIndexerClient` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `transactions` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `block` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `transactionCount` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `allTransactions` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `MockResponses` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `AccountInfo` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `balance` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `round` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assets` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `AssetHolding` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assetID` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `amount` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `TransactionResponse` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `txID` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `confirmedRound` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `confirmed` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `pending` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `Block` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `timestamp` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `NodeStatus` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `lastRound` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `timeSinceLastRound` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `LocalSandbox` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `algodPort` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `indexerPort` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `apiToken` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `workingDirectory` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `state` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `algodURL` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `indexerURL` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `start` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `stop` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `waitForReady` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `Sandbox` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `ensureRunning` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `withRunning` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `SandboxState` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `isRunning` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `isStopped` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `isTransitioning` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `description` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `stopped` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `starting` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `running` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `stopping` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `SnapshotCapture` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `capture` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `captureAll` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `captureAround` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `SnapshotStore` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `store` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `retrieve` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `compare` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `assertEqual` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `snapshotIDs` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `count` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `clear` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `remove` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `snapshots` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `StateSnapshot` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `AccountState` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `label` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `diff` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `accountState` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `SnapshotDiff` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `fromRound` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `toRound` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `balanceChanges` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `BalanceChange` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `previous` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `current` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `delta` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `increased` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `decreased` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `unchanged` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `hasChanges` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `TestTransactionBuilder` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `Defaults` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `fee` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `validRounds` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `genesisID` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `genesisHash` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `payment` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `to` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `note` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `build` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `Transaction` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `sender` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `receiver` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `firstValid` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `lastValid` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `TransactionScenarios` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `simplePayment` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `paymentWithNote` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `minimumPayment` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `largePayment` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `zeroPayment` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `highFeePayment` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `batchPayments` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |
| `circularPayments` | Existing caller-visible API preserved by the stable AlgoTest requirements and native verification lane. |

### Package Interface

The `AlgoTest` library product exposes sandbox protocols and state, account factories and pools, funded-account fixtures, transaction builders and scenarios, mock Algod and Indexer actors, snapshot capture and storage, and Algorand-specific assertion helpers.

## Invariants

1. Stateful test utilities use the existing actor and `Sendable` boundaries so concurrent tests do not introduce shared-state races.
2. Account pools release borrowed accounts according to their documented lifecycle even when a test operation fails.
3. Mock clients and snapshots remain deterministic and do not silently perform live blockchain requests.
4. Sandbox operations surface unavailable, already-running, stopped, and command failures explicitly.
5. Live sandbox or network integration remains separately configured and is not implicitly started by the blocking Trust lane.

## Behavioral Examples

```
Given deterministic funded accounts and a mock Algod client
When a test submits a transaction and captures surrounding state
Then assertions and snapshots report the existing balance and transaction changes without a live network
```

## Error Cases

| Error | When | Behavior |
|-------|------|----------|
| Sandbox unavailable | A requested local sandbox cannot be reached or managed | Return the existing sandbox error |
| Insufficient balance | A scenario cannot fund or afford the requested operation | Return an explicit balance error |
| Missing mock data | A mock query has no configured response | Return the configured mock failure |
| Missing snapshot | A requested snapshot identifier is absent | Return an explicit snapshot error |

## Dependencies

- Swift 6.0 or newer
- `swift-algorand` and `swift-algokit`
- XCTest and Foundation
- Swift-DocC plugin for independent documentation publication

## Change Log

| Version | Date | Changes |
|---------|------|---------|
| 1 | 2026-07-12 | Initial spec |
| 2026-07-13 | CHG-0002-correct-swift-algotest-governance-coverage-and-canonical-requirement-traceabilit: Correct Swift AlgoTest governance coverage and canonical requirement traceability after final migration review |
