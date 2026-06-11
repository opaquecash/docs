# Interface: SendStealthPaymentResult

Defined in: [packages/opaque/src/client.ts:423](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L423)

Result of [OpaqueClient.sendStealthPayment](../classes/OpaqueClient.md#sendstealthpayment).

## Properties

### announcePromise?

> `optional` **announcePromise?**: `Promise`\<`string`\>

Defined in: [packages/opaque/src/client.ts:433](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L433)

Pending announce tx id when `delayAnnouncement` was set: resolves after the delay
elapses and the announcement confirms. Undefined for immediate announcements.

***

### announceTxHash?

> `optional` **announceTxHash?**: `string`

Defined in: [packages/opaque/src/client.ts:428](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L428)

Separate announce tx id (Ethereum submits transfer + announce as two txs).

***

### chain

> **chain**: [`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:424](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L424)

***

### destination?

> `optional` **destination?**: `string`

Defined in: [packages/opaque/src/client.ts:437](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L437)

Solana destination account (base58) the funds were sent to.

***

### ephemeralPublicKey

> **ephemeralPublicKey**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:439](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L439)

33-byte compressed ephemeral public key (hex).

***

### metaAddressHex

> **metaAddressHex**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:441](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L441)

Resolved 66-byte recipient meta-address.

***

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:435](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L435)

EVM-style 20-byte scanner address the recipient will detect.

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:426](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L426)

Transfer tx id (Solana bundles the announce in the same tx unless delayed).
