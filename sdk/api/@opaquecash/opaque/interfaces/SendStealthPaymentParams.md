# Interface: SendStealthPaymentParams

Defined in: [packages/opaque/src/client.ts:394](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L394)

Parameters for [OpaqueClient.sendStealthPayment](../classes/OpaqueClient.md#sendstealthpayment).

## Properties

### amount

> **amount**: `bigint`

Defined in: [packages/opaque/src/client.ts:403](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L403)

Amount in base units: lamports (Solana) or wei (Ethereum native).

***

### announce?

> `optional` **announce?**: `boolean`

Defined in: [packages/opaque/src/client.ts:407](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L407)

Publish the discovery announcement (default `true`).

***

### batchId?

> `optional` **batchId?**: `number`

Defined in: [packages/opaque/src/client.ts:411](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L411)

Solana Wormhole nonce (`batch_id`) when `relay` is set.

***

### chain

> **chain**: [`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:396](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L396)

Chain to send on.

***

### delayAnnouncement?

> `optional` **delayAnnouncement?**: `number`

Defined in: [packages/opaque/src/client.ts:419](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L419)

Anonymity-set utility (guide §17): decouple send time from announce time. When set,
the value transfer is submitted immediately but the announcement is submitted only
after this many milliseconds, breaking the timing correlation between the two.
The result's `announcePromise` resolves to the announce tx id — await (or attach a
handler to) it, or the delayed announce dies with your process.

***

### recipient

> **recipient**: `string`

Defined in: [packages/opaque/src/client.ts:401](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L401)

Recipient: a 66-byte meta-address hex (used directly), a Solana base58 pubkey, or an
Ethereum `0x` address — the latter two are resolved through the chain's registry.

***

### relay?

> `optional` **relay?**: `boolean`

Defined in: [packages/opaque/src/client.ts:409](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L409)

Also relay the announcement cross-chain over Wormhole (default `false`).

***

### token?

> `optional` **token?**: `string`

Defined in: [packages/opaque/src/client.ts:405](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L405)

SPL mint / ERC-20 address; omit for native. Token sends are not yet supported (native only).
