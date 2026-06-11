# Interface: PrepareStealthSendResult

Defined in: [packages/opaque/src/client.ts:435](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L435)

Result of preparing a stealth send (ephemeral material + announce fields).

## Properties

### ephemeralPrivateKey

> **ephemeralPrivateKey**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:442](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L442)

32-byte ephemeral private key — store securely if you need ghost / later announce.

***

### ephemeralPublicKey

> **ephemeralPublicKey**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:440](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L440)

33-byte compressed ephemeral public key.

***

### metadata

> **metadata**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:444](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L444)

Metadata bytes for `announce` (view tag byte; extend with WASM for PSR).

***

### schemeId

> **schemeId**: `bigint`

Defined in: [packages/opaque/src/client.ts:436](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L436)

***

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:437](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L437)

***

### stealthPubKey

> **stealthPubKey**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:449](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L449)

Uncompressed (65-byte) stealth public-key point. Needed to derive the Solana destination
account (`deriveStealthSolanaAddress`); not required for the EVM `announce`.

***

### viewTag

> **viewTag**: `number`

Defined in: [packages/opaque/src/client.ts:438](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L438)
