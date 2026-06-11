# Interface: EvmAnnounceWithRelayResult

Defined in: [packages/opaque/src/client.ts:410](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L410)

A cross-chain `announceWithRelay` built for Ethereum (submit `{to,data,value}` via wallet).

## Properties

### chain

> **chain**: `"ethereum"`

Defined in: [packages/opaque/src/client.ts:411](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L411)

***

### chainId

> **chainId**: `number`

Defined in: [packages/opaque/src/client.ts:416](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L416)

***

### data

> **data**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:413](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L413)

***

### to

> **to**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:412](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L412)

***

### value

> **value**: `bigint`

Defined in: [packages/opaque/src/client.ts:415](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L415)

Wormhole message fee (wei) to send as `value`.
