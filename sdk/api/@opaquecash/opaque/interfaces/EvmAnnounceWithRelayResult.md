# Interface: EvmAnnounceWithRelayResult

Defined in: [packages/opaque/src/client.ts:586](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L586)

A cross-chain `announceWithRelay` built for Ethereum (submit `{to,data,value}` via wallet).

## Properties

### chain

> **chain**: `"ethereum"`

Defined in: [packages/opaque/src/client.ts:587](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L587)

***

### chainId

> **chainId**: `number`

Defined in: [packages/opaque/src/client.ts:592](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L592)

***

### data

> **data**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:589](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L589)

***

### to

> **to**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:588](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L588)

***

### value

> **value**: `bigint`

Defined in: [packages/opaque/src/client.ts:591](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L591)

Wormhole message fee (wei) to send as `value`.
