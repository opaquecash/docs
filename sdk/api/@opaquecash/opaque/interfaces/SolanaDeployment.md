# Interface: SolanaDeployment

Defined in: packages/stealth-chain-solana/dist/programs.d.ts:14

Resolved Opaque program ids for a Solana cluster.

## Properties

### attestationEngineV2

> **attestationEngineV2**: `PublicKey`

Defined in: packages/stealth-chain-solana/dist/programs.d.ts:23

PSR V2 attestation engine program.

***

### cluster

> **cluster**: [`SolanaCluster`](../type-aliases/SolanaCluster.md)

Defined in: packages/stealth-chain-solana/dist/programs.d.ts:15

***

### groth16Verifier

> **groth16Verifier**: `PublicKey`

Defined in: packages/stealth-chain-solana/dist/programs.d.ts:25

Groth16 proof verifier program.

***

### onsMirror

> **onsMirror**: `PublicKey`

Defined in: packages/stealth-chain-solana/dist/programs.d.ts:33

ONS read-only mirror program (spec/ONS.md §3).

***

### onsRegistration

> **onsRegistration**: `PublicKey`

Defined in: packages/stealth-chain-solana/dist/programs.d.ts:35

ONS Solana-originated claims program (spec/ONS.md §4.2).

***

### reputationVerifier

> **reputationVerifier**: `PublicKey`

Defined in: packages/stealth-chain-solana/dist/programs.d.ts:27

PSR reputation proof verifier program.

***

### schemaRegistry

> **schemaRegistry**: `PublicKey`

Defined in: packages/stealth-chain-solana/dist/programs.d.ts:21

PSR V2 schema registry program.

***

### stealthAnnouncer

> **stealthAnnouncer**: `PublicKey`

Defined in: packages/stealth-chain-solana/dist/programs.d.ts:19

`StealthAddressAnnouncer` program (ERC-5564 equivalent).

***

### stealthRegistry

> **stealthRegistry**: `PublicKey`

Defined in: packages/stealth-chain-solana/dist/programs.d.ts:17

`StealthMetaAddressRegistry` program (ERC-6538 equivalent).

***

### uabReceiver

> **uabReceiver**: `PublicKey`

Defined in: packages/stealth-chain-solana/dist/programs.d.ts:31

UAB receiver program (re-emits Ethereum-originated announcements from verified VAAs).

***

### wormholeCore

> **wormholeCore**: `PublicKey`

Defined in: packages/stealth-chain-solana/dist/programs.d.ts:29

Wormhole Core Bridge program (for `announce_with_relay` cross-chain announcements).
