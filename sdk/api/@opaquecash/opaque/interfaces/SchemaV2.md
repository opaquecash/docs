# Interface: SchemaV2

Defined in: packages/psr-core/dist/schema.d.ts:13

A decoded V2 schema record (chain-neutral view).

## Properties

### address

> **address**: `string`

Defined in: packages/psr-core/dist/schema.d.ts:15

Stable id (== schemaId).

***

### authority

> **authority**: `string`

Defined in: packages/psr-core/dist/schema.d.ts:19

Wallet that created the schema.

***

### createdAt

> **createdAt**: `number`

Defined in: packages/psr-core/dist/schema.d.ts:33

Block/slot when registered.

***

### delegates

> **delegates**: `string`[]

Defined in: packages/psr-core/dist/schema.d.ts:31

Authorized delegate addresses.

***

### deprecated

> **deprecated**: `boolean`

Defined in: packages/psr-core/dist/schema.d.ts:37

Whether the schema has been deprecated.

***

### fieldDefinitions

> **fieldDefinitions**: `string`

Defined in: packages/psr-core/dist/schema.d.ts:27

ABI-style field definitions, e.g. "bool passed, u64 score".

***

### name

> **name**: `string`

Defined in: packages/psr-core/dist/schema.d.ts:25

Display name.

***

### resolver

> **resolver**: `string`

Defined in: packages/psr-core/dist/schema.d.ts:21

Optional resolver (zero address = none).

***

### revocable

> **revocable**: `boolean`

Defined in: packages/psr-core/dist/schema.d.ts:23

Whether attestations can be revoked.

***

### schemaExpirySlot

> **schemaExpirySlot**: `number`

Defined in: packages/psr-core/dist/schema.d.ts:35

0 = no expiry.

***

### schemaId

> **schemaId**: `string`

Defined in: packages/psr-core/dist/schema.d.ts:17

schemaId = sha256(authority || name || version) as 0x-hex (bytes32).

***

### version

> **version**: `number`

Defined in: packages/psr-core/dist/schema.d.ts:29

Schema version (always 1 currently).
