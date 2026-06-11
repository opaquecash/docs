# Interface: IssueAttestationParams

Defined in: [packages/opaque/src/client.ts:339](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L339)

Parameters for [OpaqueClient.issueAttestation](../classes/OpaqueClient.md#issueattestation).

## Properties

### announce?

> `optional` **announce?**: `boolean`

Defined in: [packages/opaque/src/client.ts:354](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L354)

Publish a discovery announcement after issuance. Defaults to `true` when `recipient` is a
meta-address (only then is an ephemeral key available). No-op for raw-hash recipients.

***

### expiration?

> `optional` **expiration?**: [`PsrExpiryInput`](PsrExpiryInput.md)

Defined in: [packages/opaque/src/client.ts:347](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L347)

Optional attestation expiry.

***

### fieldValues

> **fieldValues**: `Record`\<`string`, `string`\>

Defined in: [packages/opaque/src/client.ts:345](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L345)

Field values keyed by field name — must match the schema's `fieldDefinitions`.

***

### recipient

> **recipient**: `string`

Defined in: [packages/opaque/src/client.ts:343](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L343)

66-byte meta-address, 20-byte stealth address, or 32-byte `stealth_address_hash` (hex).

***

### refUid?

> `optional` **refUid?**: `string`

Defined in: [packages/opaque/src/client.ts:349](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L349)

Optional reference uid (chained credential).

***

### schemaId

> **schemaId**: `string`

Defined in: [packages/opaque/src/client.ts:341](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L341)

Target schema id (`0x`-hex bytes32).
