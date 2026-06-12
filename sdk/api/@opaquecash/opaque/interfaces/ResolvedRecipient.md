# Interface: ResolvedRecipient

Defined in: [packages/opaque/src/resolve.ts:45](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/resolve.ts#L45)

Result of [OpaqueClient.resolveRecipient](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#resolverecipient).

## Properties

### input

> **input**: `string`

Defined in: [packages/opaque/src/resolve.ts:51](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/resolve.ts#L51)

The (trimmed) input that was resolved.

***

### metaAddressHex

> **metaAddressHex**: `` `0x${string}` ``

Defined in: [packages/opaque/src/resolve.ts:47](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/resolve.ts#L47)

Validated 66-byte `V‖S` meta-address (`0x` + 132 hex).

***

### source

> **source**: [`ResolvedRecipientSource`](/sdk/api/@opaquecash/opaque/type-aliases/ResolvedRecipientSource.md)

Defined in: [packages/opaque/src/resolve.ts:49](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/resolve.ts#L49)

Resolution path that produced the meta-address.
