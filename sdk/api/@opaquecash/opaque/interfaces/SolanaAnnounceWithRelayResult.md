# Interface: SolanaAnnounceWithRelayResult

Defined in: [packages/opaque/src/client.ts:486](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L486)

A cross-chain `announce_with_relay` built for Solana (sign with the wallet + extra signers).

## Properties

### chain

> **chain**: `"solana"`

Defined in: [packages/opaque/src/client.ts:487](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L487)

***

### instructions

> **instructions**: `TransactionInstruction`[]

Defined in: [packages/opaque/src/client.ts:488](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L488)

***

### signers

> **signers**: `Keypair`[]

Defined in: [packages/opaque/src/client.ts:490](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L490)

Extra signers (the fresh Wormhole message keypair) that must co-sign with the wallet.
