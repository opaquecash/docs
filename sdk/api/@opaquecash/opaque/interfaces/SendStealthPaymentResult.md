# Interface: SendStealthPaymentResult

Defined in: [packages/opaque/src/client.ts:403](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L403)

Result of [OpaqueClient.sendStealthPayment](../classes/OpaqueClient.md#sendstealthpayment).

## Properties

### announcePromise?

> `optional` **announcePromise?**: `Promise`\<`string`\>

Defined in: [packages/opaque/src/client.ts:413](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L413)

Pending announce tx id when `delayAnnouncement` was set: resolves after the delay
elapses and the announcement confirms. Undefined for immediate announcements.

***

### announceTxHash?

> `optional` **announceTxHash?**: `string`

Defined in: [packages/opaque/src/client.ts:408](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L408)

Separate announce tx id (Ethereum submits transfer + announce as two txs).

***

### chain

> **chain**: [`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:404](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L404)

***

### destination?

> `optional` **destination?**: `string`

Defined in: [packages/opaque/src/client.ts:417](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L417)

Solana destination account (base58) the funds were sent to.

***

### ephemeralPublicKey

> **ephemeralPublicKey**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:419](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L419)

33-byte compressed ephemeral public key (hex).

***

### metaAddressHex

> **metaAddressHex**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:421](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L421)

Resolved 66-byte recipient meta-address.

***

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:415](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L415)

EVM-style 20-byte scanner address the recipient will detect.

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:406](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L406)

Transfer tx id (Solana bundles the announce in the same tx unless delayed).
