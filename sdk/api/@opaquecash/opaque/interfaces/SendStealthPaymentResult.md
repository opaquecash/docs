# Interface: SendStealthPaymentResult

Defined in: [packages/opaque/src/client.ts:374](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L374)

Result of [OpaqueClient.sendStealthPayment](../classes/OpaqueClient.md#sendstealthpayment).

## Properties

### announcePromise?

> `optional` **announcePromise?**: `Promise`\<`string`\>

Defined in: [packages/opaque/src/client.ts:384](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L384)

Pending announce tx id when `delayAnnouncement` was set: resolves after the delay
elapses and the announcement confirms. Undefined for immediate announcements.

***

### announceTxHash?

> `optional` **announceTxHash?**: `string`

Defined in: [packages/opaque/src/client.ts:379](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L379)

Separate announce tx id (Ethereum submits transfer + announce as two txs).

***

### chain

> **chain**: [`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:375](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L375)

***

### destination?

> `optional` **destination?**: `string`

Defined in: [packages/opaque/src/client.ts:388](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L388)

Solana destination account (base58) the funds were sent to.

***

### ephemeralPublicKey

> **ephemeralPublicKey**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:390](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L390)

33-byte compressed ephemeral public key (hex).

***

### metaAddressHex

> **metaAddressHex**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:392](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L392)

Resolved 66-byte recipient meta-address.

***

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:386](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L386)

EVM-style 20-byte scanner address the recipient will detect.

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:377](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L377)

Transfer tx id (Solana bundles the announce in the same tx unless delayed).
