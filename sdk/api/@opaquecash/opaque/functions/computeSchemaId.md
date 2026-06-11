# Function: computeSchemaId()

> **computeSchemaId**(`authority`, `name`, `version?`): `` `0x${string}` ``

Defined in: packages/psr-core/dist/schema.d.ts:49

`schemaId = sha256(abi.encodePacked(authority, bytes(name), version))`, byte-for-byte matching
the schema registry's `computeSchemaId` on-chain.

## Parameters

### authority

`` `0x${string}` ``

### name

`string`

### version?

`number`

## Returns

`` `0x${string}` ``
