# Interface: IssueAttestationParams

Defined in: [packages/opaque/src/client.ts:290](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L290)

Parameters for [OpaqueClient.issueAttestation](../classes/OpaqueClient.md#issueattestation).

## Properties

### announce?

> `optional` **announce?**: `boolean`

Defined in: [packages/opaque/src/client.ts:305](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L305)

Publish a discovery announcement after issuance. Defaults to `true` when `recipient` is a
meta-address (only then is an ephemeral key available). No-op for raw-hash recipients.

***

### expiration?

> `optional` **expiration?**: [`PsrExpiryInput`](PsrExpiryInput.md)

Defined in: [packages/opaque/src/client.ts:298](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L298)

Optional attestation expiry.

***

### fieldValues

> **fieldValues**: `Record`\<`string`, `string`\>

Defined in: [packages/opaque/src/client.ts:296](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L296)

Field values keyed by field name — must match the schema's `fieldDefinitions`.

***

### recipient

> **recipient**: `string`

Defined in: [packages/opaque/src/client.ts:294](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L294)

66-byte meta-address, 20-byte stealth address, or 32-byte `stealth_address_hash` (hex).

***

### refUid?

> `optional` **refUid?**: `string`

Defined in: [packages/opaque/src/client.ts:300](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L300)

Optional reference uid (chained credential).

***

### schemaId

> **schemaId**: `string`

Defined in: [packages/opaque/src/client.ts:292](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L292)

Target schema id (`0x`-hex bytes32).
