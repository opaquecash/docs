# Interface: IssueAttestationParams

Defined in: [packages/opaque/src/client.ts:356](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L356)

Parameters for [OpaqueClient.issueAttestation](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#issueattestation).

## Properties

### announce?

> `optional` **announce?**: `boolean`

Defined in: [packages/opaque/src/client.ts:371](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L371)

Publish a discovery announcement after issuance. Defaults to `true` when `recipient` is a
meta-address (only then is an ephemeral key available). No-op for raw-hash recipients.

***

### expiration?

> `optional` **expiration?**: [`PsrExpiryInput`](/sdk/api/@opaquecash/opaque/interfaces/PsrExpiryInput.md)

Defined in: [packages/opaque/src/client.ts:364](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L364)

Optional attestation expiry.

***

### fieldValues

> **fieldValues**: `Record`\<`string`, `string`\>

Defined in: [packages/opaque/src/client.ts:362](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L362)

Field values keyed by field name — must match the schema's `fieldDefinitions`.

***

### recipient

> **recipient**: `string`

Defined in: [packages/opaque/src/client.ts:360](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L360)

66-byte meta-address, 20-byte stealth address, or 32-byte `stealth_address_hash` (hex).

***

### refUid?

> `optional` **refUid?**: `string`

Defined in: [packages/opaque/src/client.ts:366](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L366)

Optional reference uid (chained credential).

***

### schemaId

> **schemaId**: `string`

Defined in: [packages/opaque/src/client.ts:358](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L358)

Target schema id (`0x`-hex bytes32).
