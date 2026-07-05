# Function: computeStealthAddressAndViewTag()

> **computeStealthAddressAndViewTag**(`recipientMetaAddressHex`): `object`

Defined in: [packages/opaque/src/crypto/dksap.ts:251](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/crypto/dksap.ts#L251)

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

### solanaStealthPubKey?

> `optional` **solanaStealthPubKey?**: `Uint8Array`

32-byte ed25519 Solana stealth address point; present when the meta-address carries `S_ed`.

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

### stealthPubKeyUncompressed

> **stealthPubKeyUncompressed**: `Uint8Array`

Uncompressed (65-byte) secp256k1 stealth public-key point (Ethereum).

### viewTag

> **viewTag**: `number`
