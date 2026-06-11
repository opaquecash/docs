# Interface: EvmAnnounceWithRelayResult

Defined in: [packages/opaque/src/client.ts:439](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L439)

A cross-chain `announceWithRelay` built for Ethereum (submit `{to,data,value}` via wallet).

## Properties

### chain

> **chain**: `"ethereum"`

Defined in: [packages/opaque/src/client.ts:440](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L440)

***

### chainId

> **chainId**: `number`

Defined in: [packages/opaque/src/client.ts:445](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L445)

***

### data

> **data**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:442](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L442)

***

### to

> **to**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:441](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L441)

***

### value

> **value**: `bigint`

Defined in: [packages/opaque/src/client.ts:444](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L444)

Wormhole message fee (wei) to send as `value`.
