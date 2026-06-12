# Interface: SendStealthPaymentResult

Defined in: [packages/opaque/src/client.ts:440](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L440)

Result of [OpaqueClient.sendStealthPayment](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#sendstealthpayment).

## Properties

### announcePromise?

> `optional` **announcePromise?**: `Promise`\<`string`\>

Defined in: [packages/opaque/src/client.ts:450](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L450)

Pending announce tx id when `delayAnnouncement` was set: resolves after the delay
elapses and the announcement confirms. Undefined for immediate announcements.

***

### announceTxHash?

> `optional` **announceTxHash?**: `string`

Defined in: [packages/opaque/src/client.ts:445](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L445)

Separate announce tx id (Ethereum submits transfer + announce as two txs).

***

### chain

> **chain**: [`OpaqueScanChain`](/sdk/api/@opaquecash/opaque/type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:441](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L441)

***

### destination?

> `optional` **destination?**: `string`

Defined in: [packages/opaque/src/client.ts:454](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L454)

Solana destination account (base58) the funds were sent to.

***

### ephemeralPublicKey

> **ephemeralPublicKey**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:456](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L456)

33-byte compressed ephemeral public key (hex).

***

### metaAddressHex

> **metaAddressHex**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:458](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L458)

Resolved 66-byte recipient meta-address.

***

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:452](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L452)

EVM-style 20-byte scanner address the recipient will detect.

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:443](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L443)

Transfer tx id (Solana bundles the announce in the same tx unless delayed).
