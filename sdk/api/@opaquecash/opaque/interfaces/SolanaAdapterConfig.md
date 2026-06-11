# Interface: SolanaAdapterConfig

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:12

Construction options for [SolanaAdapter](../classes/SolanaAdapter.md).

## Properties

### cluster?

> `optional` **cluster?**: [`SolanaCluster`](../type-aliases/SolanaCluster.md)

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:18

Target cluster (default `devnet`); selects bundled program ids and the public RPC.

***

### commitment?

> `optional` **commitment?**: `Finality`

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:22

Read commitment for fetch/watch (default `confirmed`).

***

### connection?

> `optional` **connection?**: `Connection`

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:14

Pre-built connection (takes precedence over `rpcUrl`/`cluster`).

***

### deployment?

> `optional` **deployment?**: [`SolanaDeployment`](SolanaDeployment.md)

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:20

Program-id overrides (default: bundled deployment for `cluster`).

***

### rpcUrl?

> `optional` **rpcUrl?**: `string`

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:16

RPC URL to build a connection from (falls back to the cluster's public endpoint).
