# Interface: DiscoverTraitsV2Options

Defined in: [packages/opaque/src/client.ts:322](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L322)

Options for V2 schema-bound trait discovery.

## Properties

### chain

> **chain**: [`OpaqueScanChain`](/sdk/api/@opaquecash/opaque/type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:324](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L324)

Chain whose native PSR schema registry should authorize announcements.

***

### currentSlot?

> `optional` **currentSlot?**: `number` \| `bigint`

Defined in: [packages/opaque/src/client.ts:328](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L328)

Current block/slot for schema expiry checks. If omitted, it is read from the chain.

***

### schemas?

> `optional` **schemas?**: [`SchemaV2`](/sdk/api/@opaquecash/opaque/interfaces/SchemaV2.md)[]

Defined in: [packages/opaque/src/client.ts:326](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L326)

Optional pre-fetched registry snapshot. If omitted, the client fetches all schemas.

***

### trustedIssuers?

> `optional` **trustedIssuers?**: `string`[]

Defined in: [packages/opaque/src/client.ts:330](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L330)

Optional allowlist of trusted issuer identities (hex or address/base58).
