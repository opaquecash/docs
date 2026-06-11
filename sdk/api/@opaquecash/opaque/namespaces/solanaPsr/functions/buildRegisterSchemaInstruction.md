# Function: buildRegisterSchemaInstruction()

> **buildRegisterSchemaInstruction**(`params`): `TransactionInstruction`

Defined in: packages/psr-chain-solana/dist/schema.d.ts:10

## Parameters

### params

#### authority

`PublicKey`

#### fieldDefinitions

`string`

#### name

`string`

#### resolver?

`PublicKey` \| `null`

#### revocable

`boolean`

#### schemaExpirySlot

`number` \| `bigint`

#### schemaId

`Uint8Array`

#### schemaPda

`PublicKey`

#### schemaRegistryProgramId

`PublicKey`

## Returns

`TransactionInstruction`
