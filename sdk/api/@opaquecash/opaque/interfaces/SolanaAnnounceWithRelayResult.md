# Interface: SolanaAnnounceWithRelayResult

Defined in: [packages/opaque/src/client.ts:449](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L449)

A cross-chain `announce_with_relay` built for Solana (sign with the wallet + extra signers).

## Properties

### chain

> **chain**: `"solana"`

Defined in: [packages/opaque/src/client.ts:450](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L450)

***

### instructions

> **instructions**: `TransactionInstruction`[]

Defined in: [packages/opaque/src/client.ts:451](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L451)

***

### signers

> **signers**: `Keypair`[]

Defined in: [packages/opaque/src/client.ts:453](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L453)

Extra signers (the fresh Wormhole message keypair) that must co-sign with the wallet.
