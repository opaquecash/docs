# Function: buildAttestInstruction()

> **buildAttestInstruction**(`params`): `TransactionInstruction`

Defined in: packages/psr-chain-solana/dist/attestation.d.ts:8

## Parameters

### params

#### attestationPda

`PublicKey`

#### attestationProgramId

`PublicKey`

#### data

`Uint8Array`

#### expirationSlot

`number` \| `bigint`

#### issuer

`PublicKey`

#### refUid

`Uint8Array`

#### resolverProgram?

`PublicKey`

#### schemaPda

`PublicKey`

#### stealthAddressHash

`Uint8Array`

## Returns

`TransactionInstruction`
