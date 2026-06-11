# Interface: CreateSchemaParams

Defined in: [packages/opaque/src/client.ts:325](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L325)

Parameters for [OpaqueClient.createSchema](../classes/OpaqueClient.md#createschema).

## Properties

### fieldDefinitions

> **fieldDefinitions**: `string` \| [`FieldDef`](FieldDef.md)[]

Defined in: [packages/opaque/src/client.ts:329](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L329)

ABI-style string (`"bool passed, u64 score"`) or [FieldDef](FieldDef.md)s — normalized internally.

***

### name

> **name**: `string`

Defined in: [packages/opaque/src/client.ts:327](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L327)

Human-readable schema name (part of the `schemaId` preimage).

***

### resolver?

> `optional` **resolver?**: `string`

Defined in: [packages/opaque/src/client.ts:333](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L333)

Optional resolver: EVM address or Solana program pubkey. Omit for none.

***

### revocable

> **revocable**: `boolean`

Defined in: [packages/opaque/src/client.ts:331](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L331)

Whether issued attestations can be revoked (immutable after creation).

***

### schemaExpiry?

> `optional` **schemaExpiry?**: [`PsrExpiryInput`](PsrExpiryInput.md)

Defined in: [packages/opaque/src/client.ts:335](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L335)

Optional schema expiry.
