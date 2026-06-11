# Interface: IssueAttestationParams

Defined in: [packages/opaque/src/client.ts:319](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L319)

Parameters for [OpaqueClient.issueAttestation](../classes/OpaqueClient.md#issueattestation).

## Properties

### announce?

> `optional` **announce?**: `boolean`

Defined in: [packages/opaque/src/client.ts:334](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L334)

Publish a discovery announcement after issuance. Defaults to `true` when `recipient` is a
meta-address (only then is an ephemeral key available). No-op for raw-hash recipients.

***

### expiration?

> `optional` **expiration?**: [`PsrExpiryInput`](PsrExpiryInput.md)

Defined in: [packages/opaque/src/client.ts:327](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L327)

Optional attestation expiry.

***

### fieldValues

> **fieldValues**: `Record`\<`string`, `string`\>

Defined in: [packages/opaque/src/client.ts:325](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L325)

Field values keyed by field name — must match the schema's `fieldDefinitions`.

***

### recipient

> **recipient**: `string`

Defined in: [packages/opaque/src/client.ts:323](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L323)

66-byte meta-address, 20-byte stealth address, or 32-byte `stealth_address_hash` (hex).

***

### refUid?

> `optional` **refUid?**: `string`

Defined in: [packages/opaque/src/client.ts:329](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L329)

Optional reference uid (chained credential).

***

### schemaId

> **schemaId**: `string`

Defined in: [packages/opaque/src/client.ts:321](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L321)

Target schema id (`0x`-hex bytes32).
