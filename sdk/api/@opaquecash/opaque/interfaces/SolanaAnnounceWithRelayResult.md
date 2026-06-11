# Interface: SolanaAnnounceWithRelayResult

Defined in: [packages/opaque/src/client.ts:469](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L469)

A cross-chain `announce_with_relay` built for Solana (sign with the wallet + extra signers).

## Properties

### chain

> **chain**: `"solana"`

Defined in: [packages/opaque/src/client.ts:470](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L470)

***

### instructions

> **instructions**: `TransactionInstruction`[]

Defined in: [packages/opaque/src/client.ts:471](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L471)

***

### signers

> **signers**: `Keypair`[]

Defined in: [packages/opaque/src/client.ts:473](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L473)

Extra signers (the fresh Wormhole message keypair) that must co-sign with the wallet.
