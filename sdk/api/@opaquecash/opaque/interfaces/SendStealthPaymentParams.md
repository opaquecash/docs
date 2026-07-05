# Interface: SendStealthPaymentParams

Defined in: [packages/opaque/src/client.ts:465](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L465)

Parameters for [OpaqueClient.sendStealthPayment](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#sendstealthpayment).

## Properties

### amount

> **amount**: `bigint`

Defined in: [packages/opaque/src/client.ts:477](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L477)

Amount in base units: lamports / wei for the native asset, or the token's smallest unit
(raw, decimals-aware) when `token` is set.

***

### announce?

> `optional` **announce?**: `boolean`

Defined in: [packages/opaque/src/client.ts:491](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L491)

Publish the discovery announcement (default `true`).

***

### batchId?

> `optional` **batchId?**: `number`

Defined in: [packages/opaque/src/client.ts:495](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L495)

Solana Wormhole nonce (`batch_id`) when `relay` is set.

***

### chain

> **chain**: [`OpaqueScanChain`](/sdk/api/@opaquecash/opaque/type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:467](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L467)

Chain to send on.

***

### delayAnnouncement?

> `optional` **delayAnnouncement?**: `number`

Defined in: [packages/opaque/src/client.ts:503](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L503)

Anonymity-set utility (guide §17): decouple send time from announce time. When set,
the value transfer is submitted immediately but the announcement is submitted only
after this many milliseconds, breaking the timing correlation between the two.
The result's `announcePromise` resolves to the announce tx id — await (or attach a
handler to) it, or the delayed announce dies with your process.

***

### gasDrop?

> `optional` **gasDrop?**: `bigint`

Defined in: [packages/opaque/src/client.ts:489](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L489)

Optional native top-up sent to the stealth address alongside a token send, so the recipient
has gas to move the token later without a relayer. Wei (Ethereum) or lamports (Solana).
Ignored for native sends.

***

### recipient

> **recipient**: `string`

Defined in: [packages/opaque/src/client.ts:472](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L472)

Recipient: a 66-byte meta-address hex (used directly), a Solana base58 pubkey, or an
Ethereum `0x` address — the latter two are resolved through the chain's registry.

***

### relay?

> `optional` **relay?**: `boolean`

Defined in: [packages/opaque/src/client.ts:493](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L493)

Also relay the announcement cross-chain over Wormhole (default `false`).

***

### token?

> `optional` **token?**: `string`

Defined in: [packages/opaque/src/client.ts:483](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L483)

SPL mint (base58) or ERC-20 address (`0x`) to send; omit for the native asset. The recipient
receives the token at the stealth address (EVM) or that account's associated token account
(Solana); the announcement is identical to a native send.
