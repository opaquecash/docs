# Interface: EvmAnnounceWithRelayResult

Defined in: [packages/opaque/src/client.ts:459](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L459)

A cross-chain `announceWithRelay` built for Ethereum (submit `{to,data,value}` via wallet).

## Properties

### chain

> **chain**: `"ethereum"`

Defined in: [packages/opaque/src/client.ts:460](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L460)

***

### chainId

> **chainId**: `number`

Defined in: [packages/opaque/src/client.ts:465](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L465)

***

### data

> **data**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:462](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L462)

***

### to

> **to**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:461](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L461)

***

### value

> **value**: `bigint`

Defined in: [packages/opaque/src/client.ts:464](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L464)

Wormhole message fee (wei) to send as `value`.
