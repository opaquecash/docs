# Function: parseMetaAddressValue()

> **parseMetaAddressValue**(`value`): `` `0x${string}` `` \| `null`

Defined in: [packages/opaque/src/resolve.ts:74](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/resolve.ts#L74)

Parse and validate a published meta-address value: the §2.1 serialisation, optionally
`st:opq:`-prefixed. Accepts the 66-byte `V‖S` form (`0x` + 132 hex) and the 98-byte
`V‖S‖S_ed` form (`0x` + 196 hex) that adds the ed25519 Solana spend key. Returns the canonical
`0x`-form, or `null` when malformed or when either secp256k1 half (`V`, `S`) is not a valid
compressed point. The trailing 32-byte `S_ed` is an ed25519 point and is not secp-validated here.

## Parameters

### value

`string`

## Returns

`` `0x${string}` `` \| `null`
