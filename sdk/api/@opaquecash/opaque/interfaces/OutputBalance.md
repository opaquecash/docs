# Interface: OutputBalance

Defined in: [packages/opaque/src/client.ts:425](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L425)

Native balance of one owned stealth output, resolved per chain.

## Properties

### address

> **address**: `string`

Defined in: [packages/opaque/src/client.ts:433](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L433)

Account actually holding the funds: the same address on Ethereum, or the derived Solana
stealth account (base58) on Solana.

***

### chain

> **chain**: [`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:426](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L426)

***

### nativeRaw

> **nativeRaw**: `bigint`

Defined in: [packages/opaque/src/client.ts:435](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L435)

Native balance in base units (wei on Ethereum, lamports on Solana).

***

### stealthAddress

> **stealthAddress**: `string`

Defined in: [packages/opaque/src/client.ts:428](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L428)

EVM-style 20-byte scanner address the announcement was matched on.
