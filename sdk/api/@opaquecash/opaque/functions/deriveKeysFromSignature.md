# Function: deriveKeysFromSignature()

> **deriveKeysFromSignature**(`signatureHex`): `object`

Defined in: [packages/opaque/src/crypto/dksap.ts:28](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/crypto/dksap.ts#L28)

## Parameters

### signatureHex

`` `0x${string}` ``

## Returns

### solanaSpendingKey

> **solanaSpendingKey**: `Uint8Array`

32-byte seed for the ed25519 Solana spend key `s_ed` (CSAP §2.3).

### spendingKey

> **spendingKey**: `Uint8Array`

### viewingKey

> **viewingKey**: `Uint8Array`
