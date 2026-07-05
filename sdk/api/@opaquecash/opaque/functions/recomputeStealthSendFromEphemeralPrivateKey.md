# Function: recomputeStealthSendFromEphemeralPrivateKey()

> **recomputeStealthSendFromEphemeralPrivateKey**(`recipientMetaAddressHex`, `ephemeralPrivateKey`): `object`

Defined in: [packages/opaque/src/crypto/dksap.ts:302](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/crypto/dksap.ts#L302)

## Parameters

### recipientMetaAddressHex

`` `0x${string}` ``

### ephemeralPrivateKey

`Uint8Array`

## Returns

`object`

### ephemeralPriv

> **ephemeralPriv**: `Uint8Array`

### ephemeralPubKey

> **ephemeralPubKey**: `Uint8Array`

### metadata

> **metadata**: `Uint8Array`

### solanaStealthPubKey?

> `optional` **solanaStealthPubKey?**: `Uint8Array`

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

### stealthPubKeyUncompressed

> **stealthPubKeyUncompressed**: `Uint8Array`

### viewTag

> **viewTag**: `number`
