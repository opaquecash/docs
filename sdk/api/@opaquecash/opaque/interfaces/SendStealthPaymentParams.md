# Interface: SendStealthPaymentParams

Defined in: [packages/opaque/src/client.ts:345](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L345)

Parameters for [OpaqueClient.sendStealthPayment](../classes/OpaqueClient.md#sendstealthpayment).

## Properties

### amount

> **amount**: `bigint`

Defined in: [packages/opaque/src/client.ts:354](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L354)

Amount in base units: lamports (Solana) or wei (Ethereum native).

***

### announce?

> `optional` **announce?**: `boolean`

Defined in: [packages/opaque/src/client.ts:358](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L358)

Publish the discovery announcement (default `true`).

***

### batchId?

> `optional` **batchId?**: `number`

Defined in: [packages/opaque/src/client.ts:362](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L362)

Solana Wormhole nonce (`batch_id`) when `relay` is set.

***

### chain

> **chain**: [`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:347](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L347)

Chain to send on.

***

### delayAnnouncement?

> `optional` **delayAnnouncement?**: `number`

Defined in: [packages/opaque/src/client.ts:370](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L370)

Anonymity-set utility (guide §17): decouple send time from announce time. When set,
the value transfer is submitted immediately but the announcement is submitted only
after this many milliseconds, breaking the timing correlation between the two.
The result's `announcePromise` resolves to the announce tx id — await (or attach a
handler to) it, or the delayed announce dies with your process.

***

### recipient

> **recipient**: `string`

Defined in: [packages/opaque/src/client.ts:352](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L352)

Recipient: a 66-byte meta-address hex (used directly), a Solana base58 pubkey, or an
Ethereum `0x` address — the latter two are resolved through the chain's registry.

***

### relay?

> `optional` **relay?**: `boolean`

Defined in: [packages/opaque/src/client.ts:360](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L360)

Also relay the announcement cross-chain over Wormhole (default `false`).

***

### token?

> `optional` **token?**: `string`

Defined in: [packages/opaque/src/client.ts:356](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L356)

SPL mint / ERC-20 address; omit for native. Token sends are not yet supported (native only).
