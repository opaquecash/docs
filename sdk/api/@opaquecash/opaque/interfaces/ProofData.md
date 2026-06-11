# Interface: ProofData

Defined in: packages/psr-core/dist/types.d.ts:50

Groth16 proof bundle compatible with submitVerifyReputation in `@opaquecash/psr-chain`.

V2 public signals: `[merkle_root, attestation_id, external_nullifier, nullifier_hash]`.

## Properties

### attestationId

> **attestationId**: `number`

Defined in: packages/psr-core/dist/types.d.ts:59

***

### nullifier

> **nullifier**: `string`

Defined in: packages/psr-core/dist/types.d.ts:58

V2 `nullifier_hash` (`publicSignals[3]` = `Poseidon(stealth_pk, external_nullifier)`).

***

### proof

> **proof**: `object`

Defined in: packages/psr-core/dist/types.d.ts:51

#### pi\_a

> **pi\_a**: `string`[]

#### pi\_b

> **pi\_b**: `string`[][]

#### pi\_c

> **pi\_c**: `string`[]

***

### publicSignals

> **publicSignals**: `string`[]

Defined in: packages/psr-core/dist/types.d.ts:56
