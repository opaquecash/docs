# Function: buildVerifyReputationInstruction()

> **buildVerifyReputationInstruction**(`params`): `TransactionInstruction`

Defined in: packages/psr-chain-solana/dist/reputation.d.ts:33

Build a `verify_reputation` instruction. PDAs are derived by the caller (or [submitReputationProof](submitReputationProof.md)).

## Parameters

### params

#### attestationId

`number` \| `bigint`

#### configPda

`PublicKey`

#### discriminator?

`Uint8Array`

#### externalNullifier

`string` \| `bigint`

#### groth16ProgramId

`PublicKey`

#### nullifierBytes

`Uint8Array`

#### nullifierPda

`PublicKey`

#### payer

`PublicKey`

#### proofA

`Uint8Array`

#### proofB

`Uint8Array`

#### proofC

`Uint8Array`

#### reputationProgramId

`PublicKey`

#### rootBytes

`Uint8Array`

#### rootPda

`PublicKey`

## Returns

`TransactionInstruction`
