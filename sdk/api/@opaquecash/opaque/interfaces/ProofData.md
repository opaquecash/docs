# Interface: ProofData

Defined in: packages/psr-core/dist/types.d.ts:99

Groth16 proof bundle compatible with submitVerifyReputation in `@opaquecash/psr-chain`.

V2 public signals: `[merkle_root, attestation_id, external_nullifier, nullifier_hash]`.

## Properties

### attestationId

> **attestationId**: [`AttestationIdentifier`](/sdk/api/@opaquecash/opaque/type-aliases/AttestationIdentifier.md)

Defined in: packages/psr-core/dist/types.d.ts:108

***

### nullifier

> **nullifier**: `string`

Defined in: packages/psr-core/dist/types.d.ts:107

V2 `nullifier_hash` (`publicSignals[3]` = `Poseidon(stealth_pk, external_nullifier)`).

***

### proof

> **proof**: `object`

Defined in: packages/psr-core/dist/types.d.ts:100

#### pi\_a

> **pi\_a**: `string`[]

#### pi\_b

> **pi\_b**: `string`[][]

#### pi\_c

> **pi\_c**: `string`[]

***

### publicSignals

> **publicSignals**: `string`[]

Defined in: packages/psr-core/dist/types.d.ts:105
