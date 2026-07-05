# Function: ipfsPathFromInput()

> **ipfsPathFromInput**(`input`): `string` \| `null`

Defined in: [packages/opaque/src/resolve.ts:164](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/resolve.ts#L164)

Extract the `<cid>[/path]` from an `ipfs://` URI, an `/ipfs/` gateway path, or a
bare CID (v0 `Qm…` base58 or v1 base32). Returns `null` when the input is not IPFS-shaped.

## Parameters

### input

`string`

## Returns

`string` \| `null`
