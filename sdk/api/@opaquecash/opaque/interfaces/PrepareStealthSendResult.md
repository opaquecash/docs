# Interface: PrepareStealthSendResult

Defined in: [packages/opaque/src/client.ts:611](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L611)

Result of preparing a stealth send (ephemeral material + announce fields).

## Properties

### ephemeralPrivateKey

> **ephemeralPrivateKey**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:618](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L618)

32-byte ephemeral private key — store securely if you need ghost / later announce.

***

### ephemeralPublicKey

> **ephemeralPublicKey**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:616](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L616)

33-byte compressed ephemeral public key.

***

### metadata

> **metadata**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:620](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L620)

Metadata bytes for `announce` (view tag byte; extend with WASM for PSR).

***

### schemeId

> **schemeId**: `bigint`

Defined in: [packages/opaque/src/client.ts:612](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L612)

***

### solanaStealthPubKey?

> `optional` **solanaStealthPubKey?**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:629](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L629)

32-byte ed25519 Solana stealth address point. Needed to derive the Solana destination
(`deriveStealthSolanaAddress`); present only when the recipient meta-address carries `S_ed`.

***

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:613](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L613)

***

### stealthPubKey

> **stealthPubKey**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:624](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L624)

Uncompressed (65-byte) secp256k1 stealth public-key point (Ethereum); not required for `announce`.

***

### viewTag

> **viewTag**: `number`

Defined in: [packages/opaque/src/client.ts:614](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L614)
