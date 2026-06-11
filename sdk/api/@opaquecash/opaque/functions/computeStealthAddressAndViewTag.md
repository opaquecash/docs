# Function: computeStealthAddressAndViewTag()

> **computeStealthAddressAndViewTag**(`recipientMetaAddressHex`): `object`

Defined in: [packages/opaque/src/crypto/dksap.ts:136](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/crypto/dksap.ts#L136)

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
