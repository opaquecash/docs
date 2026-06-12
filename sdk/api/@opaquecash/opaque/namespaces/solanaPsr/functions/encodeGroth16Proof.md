# Function: encodeGroth16Proof()

> **encodeGroth16Proof**(`proof`): `object`

Defined in: packages/psr-chain-solana/dist/reputation.d.ts:25

Flatten a Groth16 proof into the verifier's 64/128/64-byte big-endian layout.

## Parameters

### proof

[`Groth16ProofInput`](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/interfaces/Groth16ProofInput.md)

## Returns

`object`

### proofA

> **proofA**: `Uint8Array`

### proofB

> **proofB**: `Uint8Array`

### proofC

> **proofC**: `Uint8Array`
