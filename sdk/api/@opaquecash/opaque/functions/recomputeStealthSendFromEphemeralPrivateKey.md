# Function: recomputeStealthSendFromEphemeralPrivateKey()

> **recomputeStealthSendFromEphemeralPrivateKey**(`recipientMetaAddressHex`, `ephemeralPrivateKey`): `object`

Defined in: [packages/opaque/src/crypto/dksap.ts:181](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/crypto/dksap.ts#L181)

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

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

### stealthPubKeyUncompressed

> **stealthPubKeyUncompressed**: `Uint8Array`

### viewTag

> **viewTag**: `number`
