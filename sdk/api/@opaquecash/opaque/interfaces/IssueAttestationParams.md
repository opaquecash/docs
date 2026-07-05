# Interface: IssueAttestationParams

Defined in: [packages/opaque/src/client.ts:410](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L410)

Parameters for [OpaqueClient.issueAttestation](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#issueattestation).

## Properties

### announce?

> `optional` **announce?**: `boolean`

Defined in: [packages/opaque/src/client.ts:425](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L425)

Publish a discovery announcement after issuance. Defaults to `true` when `recipient` is a
meta-address (only then is an ephemeral key available). No-op for raw-hash recipients.

***

### expiration?

> `optional` **expiration?**: [`PsrExpiryInput`](/sdk/api/@opaquecash/opaque/interfaces/PsrExpiryInput.md)

Defined in: [packages/opaque/src/client.ts:418](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L418)

Optional attestation expiry.

***

### fieldValues

> **fieldValues**: `Record`\<`string`, `string`\>

Defined in: [packages/opaque/src/client.ts:416](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L416)

Field values keyed by field name — must match the schema's `fieldDefinitions`.

***

### recipient

> **recipient**: `string`

Defined in: [packages/opaque/src/client.ts:414](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L414)

66-byte meta-address, 20-byte stealth address, or 32-byte `stealth_address_hash` (hex).

***

### refUid?

> `optional` **refUid?**: `string`

Defined in: [packages/opaque/src/client.ts:420](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L420)

Optional reference uid (chained credential).

***

### schemaId

> **schemaId**: `string`

Defined in: [packages/opaque/src/client.ts:412](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L412)

Target schema id (`0x`-hex bytes32).
