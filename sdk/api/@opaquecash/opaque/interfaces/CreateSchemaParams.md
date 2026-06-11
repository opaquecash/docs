# Interface: CreateSchemaParams

Defined in: [packages/opaque/src/client.ts:305](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L305)

Parameters for [OpaqueClient.createSchema](../classes/OpaqueClient.md#createschema).

## Properties

### fieldDefinitions

> **fieldDefinitions**: `string` \| [`FieldDef`](FieldDef.md)[]

Defined in: [packages/opaque/src/client.ts:309](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L309)

ABI-style string (`"bool passed, u64 score"`) or [FieldDef](FieldDef.md)s — normalized internally.

***

### name

> **name**: `string`

Defined in: [packages/opaque/src/client.ts:307](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L307)

Human-readable schema name (part of the `schemaId` preimage).

***

### resolver?

> `optional` **resolver?**: `string`

Defined in: [packages/opaque/src/client.ts:313](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L313)

Optional resolver: EVM address or Solana program pubkey. Omit for none.

***

### revocable

> **revocable**: `boolean`

Defined in: [packages/opaque/src/client.ts:311](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L311)

Whether issued attestations can be revoked (immutable after creation).

***

### schemaExpiry?

> `optional` **schemaExpiry?**: [`PsrExpiryInput`](PsrExpiryInput.md)

Defined in: [packages/opaque/src/client.ts:315](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L315)

Optional schema expiry.
