# Function: encodeAttestationData()

> **encodeAttestationData**(`fieldValues`, `fieldDefs`): `` `0x${string}` ``

Defined in: packages/psr-core/dist/attestation.d.ts:47

Encode field values: per field a 4-byte LE length prefix followed by UTF-8 bytes.

## Parameters

### fieldValues

`Record`\<`string`, `string`\>

### fieldDefs

readonly [`AttestationField`](../type-aliases/AttestationField.md)[]

## Returns

`` `0x${string}` ``
