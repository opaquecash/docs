# Function: computeStealthAddressAndViewTag()

> **computeStealthAddressAndViewTag**(`recipientMetaAddressHex`): `object`

Defined in: [packages/opaque/src/crypto/dksap.ts:136](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/crypto/dksap.ts#L136)

## Parameters

### recipientMetaAddressHex

`` `0x${string}` ``

## Returns

### ephemeralPriv

> **ephemeralPriv**: `Uint8Array`

### ephemeralPubKey

> **ephemeralPubKey**: `Uint8Array`

### metadata

> **metadata**: `Uint8Array`

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

### stealthPubKeyUncompressed

> **stealthPubKeyUncompressed**: `Uint8Array`

Uncompressed (65-byte) stealth public-key point; used to derive the Solana destination.

### viewTag

> **viewTag**: `number`
