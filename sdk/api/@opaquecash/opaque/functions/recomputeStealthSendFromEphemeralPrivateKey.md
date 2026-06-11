# Function: recomputeStealthSendFromEphemeralPrivateKey()

> **recomputeStealthSendFromEphemeralPrivateKey**(`recipientMetaAddressHex`, `ephemeralPrivateKey`): `object`

Defined in: [packages/opaque/src/crypto/dksap.ts:181](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/crypto/dksap.ts#L181)

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
