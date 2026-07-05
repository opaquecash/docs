# Interface: SolanaAdapterConfig

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:13

Construction options for [SolanaAdapter](/sdk/api/@opaquecash/opaque/classes/SolanaAdapter.md).

## Properties

### cluster?

> `optional` **cluster?**: [`SolanaCluster`](/sdk/api/@opaquecash/opaque/type-aliases/SolanaCluster.md)

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:19

Target cluster (default `devnet`); selects bundled program ids and the public RPC.

***

### commitment?

> `optional` **commitment?**: `Finality`

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:23

Read commitment for fetch/watch (default `confirmed`).

***

### connection?

> `optional` **connection?**: `Connection`

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:15

Pre-built connection (takes precedence over `rpcUrl`/`cluster`).

***

### deployment?

> `optional` **deployment?**: [`SolanaDeployment`](/sdk/api/@opaquecash/opaque/interfaces/SolanaDeployment.md)

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:21

Program-id overrides (default: bundled deployment for `cluster`).

***

### rpcUrl?

> `optional` **rpcUrl?**: `string`

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:17

RPC URL to build a connection from (falls back to the cluster's public endpoint).
