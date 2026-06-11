# Function: computeSchemaId()

> **computeSchemaId**(`authority`, `name`, `version?`): `Uint8Array`

Defined in: packages/psr-chain-solana/dist/schema.d.ts:7

`schema_id = sha256(authority_bytes(32) || utf8(name) || [version])`.

## Parameters

### authority

`PublicKey`

### name

`string`

### version?

`number`

## Returns

`Uint8Array`
