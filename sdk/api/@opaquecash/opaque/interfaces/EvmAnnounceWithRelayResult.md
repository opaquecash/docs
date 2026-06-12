# Interface: EvmAnnounceWithRelayResult

Defined in: [packages/opaque/src/client.ts:476](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L476)

A cross-chain `announceWithRelay` built for Ethereum (submit `{to,data,value}` via wallet).

## Properties

### chain

> **chain**: `"ethereum"`

Defined in: [packages/opaque/src/client.ts:477](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L477)

***

### chainId

> **chainId**: `number`

Defined in: [packages/opaque/src/client.ts:482](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L482)

***

### data

> **data**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:479](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L479)

***

### to

> **to**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:478](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L478)

***

### value

> **value**: `bigint`

Defined in: [packages/opaque/src/client.ts:481](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L481)

Wormhole message fee (wei) to send as `value`.
