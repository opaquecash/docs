# Interface: SolanaAnnounceWithRelayResult

Defined in: [packages/opaque/src/client.ts:420](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L420)

A cross-chain `announce_with_relay` built for Solana (sign with the wallet + extra signers).

## Properties

### chain

> **chain**: `"solana"`

Defined in: [packages/opaque/src/client.ts:421](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L421)

***

### instructions

> **instructions**: `TransactionInstruction`[]

Defined in: [packages/opaque/src/client.ts:422](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L422)

***

### signers

> **signers**: `Keypair`[]

Defined in: [packages/opaque/src/client.ts:424](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L424)

Extra signers (the fresh Wormhole message keypair) that must co-sign with the wallet.
