# Interface: PrepareStealthSendResult

Defined in: [packages/opaque/src/client.ts:484](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L484)

Result of preparing a stealth send (ephemeral material + announce fields).

## Properties

### ephemeralPrivateKey

> **ephemeralPrivateKey**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:491](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L491)

32-byte ephemeral private key — store securely if you need ghost / later announce.

***

### ephemeralPublicKey

> **ephemeralPublicKey**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:489](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L489)

33-byte compressed ephemeral public key.

***

### metadata

> **metadata**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:493](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L493)

Metadata bytes for `announce` (view tag byte; extend with WASM for PSR).

***

### schemeId

> **schemeId**: `bigint`

Defined in: [packages/opaque/src/client.ts:485](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L485)

***

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:486](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L486)

***

### stealthPubKey

> **stealthPubKey**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:498](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L498)

Uncompressed (65-byte) stealth public-key point. Needed to derive the Solana destination
account (`deriveStealthSolanaAddress`); not required for the EVM `announce`.

***

### viewTag

> **viewTag**: `number`

Defined in: [packages/opaque/src/client.ts:487](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L487)
