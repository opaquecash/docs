# Interface: CreateSchemaParams

Defined in: [packages/opaque/src/client.ts:276](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L276)

Parameters for [OpaqueClient.createSchema](../classes/OpaqueClient.md#createschema).

## Properties

### fieldDefinitions

> **fieldDefinitions**: `string` \| [`FieldDef`](FieldDef.md)[]

Defined in: [packages/opaque/src/client.ts:280](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L280)

ABI-style string (`"bool passed, u64 score"`) or [FieldDef](FieldDef.md)s — normalized internally.

***

### name

> **name**: `string`

Defined in: [packages/opaque/src/client.ts:278](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L278)

Human-readable schema name (part of the `schemaId` preimage).

***

### resolver?

> `optional` **resolver?**: `string`

Defined in: [packages/opaque/src/client.ts:284](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L284)

Optional resolver: EVM address or Solana program pubkey. Omit for none.

***

### revocable

> **revocable**: `boolean`

Defined in: [packages/opaque/src/client.ts:282](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L282)

Whether issued attestations can be revoked (immutable after creation).

***

### schemaExpiry?

> `optional` **schemaExpiry?**: [`PsrExpiryInput`](PsrExpiryInput.md)

Defined in: [packages/opaque/src/client.ts:286](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L286)

Optional schema expiry.
