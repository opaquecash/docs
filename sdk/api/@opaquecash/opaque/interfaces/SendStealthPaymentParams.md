# Interface: SendStealthPaymentParams

Defined in: [packages/opaque/src/client.ts:374](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L374)

Parameters for [OpaqueClient.sendStealthPayment](../classes/OpaqueClient.md#sendstealthpayment).

## Properties

### amount

> **amount**: `bigint`

Defined in: [packages/opaque/src/client.ts:383](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L383)

Amount in base units: lamports (Solana) or wei (Ethereum native).

***

### announce?

> `optional` **announce?**: `boolean`

Defined in: [packages/opaque/src/client.ts:387](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L387)

Publish the discovery announcement (default `true`).

***

### batchId?

> `optional` **batchId?**: `number`

Defined in: [packages/opaque/src/client.ts:391](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L391)

Solana Wormhole nonce (`batch_id`) when `relay` is set.

***

### chain

> **chain**: [`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:376](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L376)

Chain to send on.

***

### delayAnnouncement?

> `optional` **delayAnnouncement?**: `number`

Defined in: [packages/opaque/src/client.ts:399](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L399)

Anonymity-set utility (guide §17): decouple send time from announce time. When set,
the value transfer is submitted immediately but the announcement is submitted only
after this many milliseconds, breaking the timing correlation between the two.
The result's `announcePromise` resolves to the announce tx id — await (or attach a
handler to) it, or the delayed announce dies with your process.

***

### recipient

> **recipient**: `string`

Defined in: [packages/opaque/src/client.ts:381](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L381)

Recipient: a 66-byte meta-address hex (used directly), a Solana base58 pubkey, or an
Ethereum `0x` address — the latter two are resolved through the chain's registry.

***

### relay?

> `optional` **relay?**: `boolean`

Defined in: [packages/opaque/src/client.ts:389](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L389)

Also relay the announcement cross-chain over Wormhole (default `false`).

***

### token?

> `optional` **token?**: `string`

Defined in: [packages/opaque/src/client.ts:385](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L385)

SPL mint / ERC-20 address; omit for native. Token sends are not yet supported (native only).
