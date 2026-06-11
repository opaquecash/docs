# Function: submitReputationProof()

> **submitReputationProof**(`connection`, `params`): `Promise`\<`string`\>

Defined in: packages/psr-chain-solana/dist/reputation.d.ts:53

Submit a reputation proof to the verifier: derives PDAs, checks the root is registered and the
nullifier is unused, builds the instruction, then signs (via `signTransaction`) and sends.

## Parameters

### connection

`Connection`

### params

#### attestationId

`number` \| `bigint`

#### externalNullifier

`string` \| `bigint`

#### groth16ProgramId

`PublicKey`

#### merkleRoot

`string` \| `bigint`

Merkle root as a decimal string or bigint (field element).

#### nullifier

`string` \| `bigint`

V2 `nullifier_hash` public input (`publicSignals[3]` =
`Poseidon(stealth_pk, external_nullifier)`) as a decimal string or bigint.

#### proof

[`Groth16ProofInput`](../interfaces/Groth16ProofInput.md)

#### publicKey

`PublicKey`

#### reputationProgramId

`PublicKey`

#### signTransaction

(`tx`) => `Promise`\<`Transaction`\>

## Returns

`Promise`\<`string`\>
