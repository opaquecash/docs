# Interface: ResolvedRecipient

Defined in: [packages/opaque/src/resolve.ts:39](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/resolve.ts#L39)

Result of [OpaqueClient.resolveRecipient](../classes/OpaqueClient.md#resolverecipient).

## Properties

### input

> **input**: `string`

Defined in: [packages/opaque/src/resolve.ts:45](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/resolve.ts#L45)

The (trimmed) input that was resolved.

***

### metaAddressHex

> **metaAddressHex**: `` `0x${string}` ``

Defined in: [packages/opaque/src/resolve.ts:41](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/resolve.ts#L41)

Validated 66-byte `V‖S` meta-address (`0x` + 132 hex).

***

### source

> **source**: [`ResolvedRecipientSource`](../type-aliases/ResolvedRecipientSource.md)

Defined in: [packages/opaque/src/resolve.ts:43](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/resolve.ts#L43)

Resolution path that produced the meta-address.
