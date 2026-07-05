# Interface: DiscoverTraitsV2Options

Defined in: [packages/opaque/src/client.ts:376](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L376)

Options for V2 schema-bound trait discovery.

## Properties

### chain

> **chain**: [`OpaqueScanChain`](/sdk/api/@opaquecash/opaque/type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:378](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L378)

Chain whose native PSR schema registry should authorize announcements.

***

### currentSlot?

> `optional` **currentSlot?**: `number` \| `bigint`

Defined in: [packages/opaque/src/client.ts:382](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L382)

Current block/slot for schema expiry checks. If omitted, it is read from the chain.

***

### schemas?

> `optional` **schemas?**: [`SchemaV2`](/sdk/api/@opaquecash/opaque/interfaces/SchemaV2.md)[]

Defined in: [packages/opaque/src/client.ts:380](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L380)

Optional pre-fetched registry snapshot. If omitted, the client fetches all schemas.

***

### trustedIssuers?

> `optional` **trustedIssuers?**: `string`[]

Defined in: [packages/opaque/src/client.ts:384](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L384)

Optional allowlist of trusted issuer identities (hex or address/base58).
