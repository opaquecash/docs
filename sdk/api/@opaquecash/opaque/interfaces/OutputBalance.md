# Interface: OutputBalance

Defined in: [packages/opaque/src/client.ts:396](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L396)

Native balance of one owned stealth output, resolved per chain.

## Properties

### address

> **address**: `string`

Defined in: [packages/opaque/src/client.ts:404](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L404)

Account actually holding the funds: the same address on Ethereum, or the derived Solana
stealth account (base58) on Solana.

***

### chain

> **chain**: [`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:397](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L397)

***

### nativeRaw

> **nativeRaw**: `bigint`

Defined in: [packages/opaque/src/client.ts:406](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L406)

Native balance in base units (wei on Ethereum, lamports on Solana).

***

### stealthAddress

> **stealthAddress**: `string`

Defined in: [packages/opaque/src/client.ts:399](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L399)

EVM-style 20-byte scanner address the announcement was matched on.
