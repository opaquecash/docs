# Function: encodeV2AttestationMetadata()

> **encodeV2AttestationMetadata**(`args`): `` `0x${string}` ``

Defined in: packages/psr-core/dist/attestation.d.ts:55

Build the `announce` metadata for a V2 attestation:
`viewTag(1) || 0xB2 || schemaId(32) || issuer(32) || uid(32) || nonce(32)` (130 bytes).
The recipient's scanner matches it with their viewing key.

## Parameters

### args

#### issuer

`` `0x${string}` ``

#### nonce

`` `0x${string}` ``

#### schemaId

`` `0x${string}` ``

#### uid

`` `0x${string}` ``

#### viewTag

`number`

## Returns

`` `0x${string}` ``
