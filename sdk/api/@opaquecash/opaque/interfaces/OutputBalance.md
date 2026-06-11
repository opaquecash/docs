# Interface: OutputBalance

Defined in: [packages/opaque/src/client.ts:445](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L445)

Native balance of one owned stealth output, resolved per chain.

## Properties

### address

> **address**: `string`

Defined in: [packages/opaque/src/client.ts:453](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L453)

Account actually holding the funds: the same address on Ethereum, or the derived Solana
stealth account (base58) on Solana.

***

### chain

> **chain**: [`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:446](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L446)

***

### nativeRaw

> **nativeRaw**: `bigint`

Defined in: [packages/opaque/src/client.ts:455](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L455)

Native balance in base units (wei on Ethereum, lamports on Solana).

***

### stealthAddress

> **stealthAddress**: `string`

Defined in: [packages/opaque/src/client.ts:448](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L448)

EVM-style 20-byte scanner address the announcement was matched on.
