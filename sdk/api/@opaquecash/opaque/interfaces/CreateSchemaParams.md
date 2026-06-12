# Interface: CreateSchemaParams

Defined in: [packages/opaque/src/client.ts:342](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L342)

Parameters for [OpaqueClient.createSchema](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#createschema).

## Properties

### fieldDefinitions

> **fieldDefinitions**: `string` \| [`FieldDef`](/sdk/api/@opaquecash/opaque/interfaces/FieldDef.md)[]

Defined in: [packages/opaque/src/client.ts:346](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L346)

ABI-style string (`"bool passed, u64 score"`) or [FieldDef](/sdk/api/@opaquecash/opaque/interfaces/FieldDef.md)s — normalized internally.

***

### name

> **name**: `string`

Defined in: [packages/opaque/src/client.ts:344](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L344)

Human-readable schema name (part of the `schemaId` preimage).

***

### resolver?

> `optional` **resolver?**: `string`

Defined in: [packages/opaque/src/client.ts:350](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L350)

Optional resolver: EVM address or Solana program pubkey. Omit for none.

***

### revocable

> **revocable**: `boolean`

Defined in: [packages/opaque/src/client.ts:348](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L348)

Whether issued attestations can be revoked (immutable after creation).

***

### schemaExpiry?

> `optional` **schemaExpiry?**: [`PsrExpiryInput`](/sdk/api/@opaquecash/opaque/interfaces/PsrExpiryInput.md)

Defined in: [packages/opaque/src/client.ts:352](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L352)

Optional schema expiry.
