# Interface: CreateSchemaParams

Defined in: [packages/opaque/src/client.ts:396](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L396)

Parameters for [OpaqueClient.createSchema](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#createschema).

## Properties

### fieldDefinitions

> **fieldDefinitions**: `string` \| [`FieldDef`](/sdk/api/@opaquecash/opaque/interfaces/FieldDef.md)[]

Defined in: [packages/opaque/src/client.ts:400](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L400)

ABI-style string (`"bool passed, u64 score"`) or [FieldDef](/sdk/api/@opaquecash/opaque/interfaces/FieldDef.md)s — normalized internally.

***

### name

> **name**: `string`

Defined in: [packages/opaque/src/client.ts:398](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L398)

Human-readable schema name (part of the `schemaId` preimage).

***

### resolver?

> `optional` **resolver?**: `string`

Defined in: [packages/opaque/src/client.ts:404](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L404)

Optional resolver: EVM address or Solana program pubkey. Omit for none.

***

### revocable

> **revocable**: `boolean`

Defined in: [packages/opaque/src/client.ts:402](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L402)

Whether issued attestations can be revoked (immutable after creation).

***

### schemaExpiry?

> `optional` **schemaExpiry?**: [`PsrExpiryInput`](/sdk/api/@opaquecash/opaque/interfaces/PsrExpiryInput.md)

Defined in: [packages/opaque/src/client.ts:406](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L406)

Optional schema expiry.
