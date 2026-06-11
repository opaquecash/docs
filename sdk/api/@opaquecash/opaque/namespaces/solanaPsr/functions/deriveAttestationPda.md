# Function: deriveAttestationPda()

> **deriveAttestationPda**(`attestationProgramId`, `schemaId`, `issuer`, `stealthAddressHash`): `PublicKey`

Defined in: packages/psr-chain-solana/dist/attestation.d.ts:7

Derive the AttestationPDA: `["attestation_v2", schemaId, issuer, stealthAddressHash]`.

## Parameters

### attestationProgramId

`PublicKey`

### schemaId

`Uint8Array`

### issuer

`PublicKey`

### stealthAddressHash

`Uint8Array`

## Returns

`PublicKey`
