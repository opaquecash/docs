# Interface: SendStealthPaymentParams

Defined in: [packages/opaque/src/client.ts:411](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L411)

Parameters for [OpaqueClient.sendStealthPayment](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#sendstealthpayment).

## Properties

### amount

> **amount**: `bigint`

Defined in: [packages/opaque/src/client.ts:420](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L420)

Amount in base units: lamports (Solana) or wei (Ethereum native).

***

### announce?

> `optional` **announce?**: `boolean`

Defined in: [packages/opaque/src/client.ts:424](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L424)

Publish the discovery announcement (default `true`).

***

### batchId?

> `optional` **batchId?**: `number`

Defined in: [packages/opaque/src/client.ts:428](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L428)

Solana Wormhole nonce (`batch_id`) when `relay` is set.

***

### chain

> **chain**: [`OpaqueScanChain`](/sdk/api/@opaquecash/opaque/type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:413](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L413)

Chain to send on.

***

### delayAnnouncement?

> `optional` **delayAnnouncement?**: `number`

Defined in: [packages/opaque/src/client.ts:436](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L436)

Anonymity-set utility (guide §17): decouple send time from announce time. When set,
the value transfer is submitted immediately but the announcement is submitted only
after this many milliseconds, breaking the timing correlation between the two.
The result's `announcePromise` resolves to the announce tx id — await (or attach a
handler to) it, or the delayed announce dies with your process.

***

### recipient

> **recipient**: `string`

Defined in: [packages/opaque/src/client.ts:418](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L418)

Recipient: a 66-byte meta-address hex (used directly), a Solana base58 pubkey, or an
Ethereum `0x` address — the latter two are resolved through the chain's registry.

***

### relay?

> `optional` **relay?**: `boolean`

Defined in: [packages/opaque/src/client.ts:426](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L426)

Also relay the announcement cross-chain over Wormhole (default `false`).

***

### token?

> `optional` **token?**: `string`

Defined in: [packages/opaque/src/client.ts:422](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L422)

SPL mint / ERC-20 address; omit for native. Token sends are not yet supported (native only).
