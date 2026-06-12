# Interface: OutputBalance

Defined in: [packages/opaque/src/client.ts:462](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L462)

Native balance of one owned stealth output, resolved per chain.

## Properties

### address

> **address**: `string`

Defined in: [packages/opaque/src/client.ts:470](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L470)

Account actually holding the funds: the same address on Ethereum, or the derived Solana
stealth account (base58) on Solana.

***

### chain

> **chain**: [`OpaqueScanChain`](/sdk/api/@opaquecash/opaque/type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:463](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L463)

***

### nativeRaw

> **nativeRaw**: `bigint`

Defined in: [packages/opaque/src/client.ts:472](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L472)

Native balance in base units (wei on Ethereum, lamports on Solana).

***

### stealthAddress

> **stealthAddress**: `string`

Defined in: [packages/opaque/src/client.ts:465](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L465)

EVM-style 20-byte scanner address the announcement was matched on.
