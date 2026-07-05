# Interface: SolanaAnnounceWithRelayResult

Defined in: [packages/opaque/src/client.ts:596](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L596)

A cross-chain `announce_with_relay` built for Solana (sign with the wallet + extra signers).

## Properties

### chain

> **chain**: `"solana"`

Defined in: [packages/opaque/src/client.ts:597](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L597)

***

### instructions

> **instructions**: `TransactionInstruction`[]

Defined in: [packages/opaque/src/client.ts:598](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L598)

***

### signers

> **signers**: `Keypair`[]

Defined in: [packages/opaque/src/client.ts:600](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L600)

Extra signers (the fresh Wormhole message keypair) that must co-sign with the wallet.
