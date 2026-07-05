# Interface: OutputBalance

Defined in: [packages/opaque/src/client.ts:529](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L529)

Native balance of one owned stealth output, resolved per chain.

## Properties

### address

> **address**: `string`

Defined in: [packages/opaque/src/client.ts:537](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L537)

Account actually holding the funds: the same address on Ethereum, or the derived Solana
stealth account (base58) on Solana.

***

### chain

> **chain**: [`OpaqueScanChain`](/sdk/api/@opaquecash/opaque/type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:530](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L530)

***

### nativeRaw

> **nativeRaw**: `bigint`

Defined in: [packages/opaque/src/client.ts:539](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L539)

Native balance in base units (wei on Ethereum, lamports on Solana).

***

### stealthAddress

> **stealthAddress**: `string`

Defined in: [packages/opaque/src/client.ts:532](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L532)

EVM-style 20-byte scanner address the announcement was matched on.
