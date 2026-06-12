# Interface: PrepareStealthSendResult

Defined in: [packages/opaque/src/client.ts:501](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L501)

Result of preparing a stealth send (ephemeral material + announce fields).

## Properties

### ephemeralPrivateKey

> **ephemeralPrivateKey**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:508](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L508)

32-byte ephemeral private key — store securely if you need ghost / later announce.

***

### ephemeralPublicKey

> **ephemeralPublicKey**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:506](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L506)

33-byte compressed ephemeral public key.

***

### metadata

> **metadata**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:510](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L510)

Metadata bytes for `announce` (view tag byte; extend with WASM for PSR).

***

### schemeId

> **schemeId**: `bigint`

Defined in: [packages/opaque/src/client.ts:502](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L502)

***

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:503](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L503)

***

### stealthPubKey

> **stealthPubKey**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:515](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L515)

Uncompressed (65-byte) stealth public-key point. Needed to derive the Solana destination
account (`deriveStealthSolanaAddress`); not required for the EVM `announce`.

***

### viewTag

> **viewTag**: `number`

Defined in: [packages/opaque/src/client.ts:504](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L504)
