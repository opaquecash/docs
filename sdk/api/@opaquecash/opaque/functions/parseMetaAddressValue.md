# Function: parseMetaAddressValue()

> **parseMetaAddressValue**(`value`): `` `0x${string}` `` \| `null`

Defined in: [packages/opaque/src/resolve.ts:73](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/resolve.ts#L73)

Parse and validate a published meta-address value: the §2.1 serialisation
(`0x` + 132 hex, `V‖S`), optionally `st:opq:`-prefixed. Returns the canonical
`0x`-form, or `null` when malformed or when either 33-byte half is not a valid
compressed secp256k1 point.

## Parameters

### value

`string`

## Returns

`` `0x${string}` `` \| `null`
