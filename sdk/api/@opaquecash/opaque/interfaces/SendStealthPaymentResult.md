# Interface: SendStealthPaymentResult

Defined in: [packages/opaque/src/client.ts:507](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L507)

Result of [OpaqueClient.sendStealthPayment](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#sendstealthpayment).

## Properties

### announcePromise?

> `optional` **announcePromise?**: `Promise`\<`string`\>

Defined in: [packages/opaque/src/client.ts:517](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L517)

Pending announce tx id when `delayAnnouncement` was set: resolves after the delay
elapses and the announcement confirms. Undefined for immediate announcements.

***

### announceTxHash?

> `optional` **announceTxHash?**: `string`

Defined in: [packages/opaque/src/client.ts:512](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L512)

Separate announce tx id (Ethereum submits transfer + announce as two txs).

***

### chain

> **chain**: [`OpaqueScanChain`](/sdk/api/@opaquecash/opaque/type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:508](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L508)

***

### destination?

> `optional` **destination?**: `string`

Defined in: [packages/opaque/src/client.ts:521](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L521)

Solana destination account (base58) the funds were sent to.

***

### ephemeralPublicKey

> **ephemeralPublicKey**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:523](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L523)

33-byte compressed ephemeral public key (hex).

***

### metaAddressHex

> **metaAddressHex**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:525](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L525)

Resolved 66-byte recipient meta-address.

***

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:519](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L519)

EVM-style 20-byte scanner address the recipient will detect.

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:510](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L510)

Transfer tx id (Solana bundles the announce in the same tx unless delayed).
