# Function: ipfsPathFromInput()

> **ipfsPathFromInput**(`input`): `string` \| `null`

Defined in: [packages/opaque/src/resolve.ts:163](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/resolve.ts#L163)

Extract the `<cid>[/path]` from an `ipfs://` URI, an `/ipfs/` gateway path, or a
bare CID (v0 `Qm…` base58 or v1 base32). Returns `null` when the input is not IPFS-shaped.

## Parameters

### input

`string`

## Returns

`string` \| `null`
