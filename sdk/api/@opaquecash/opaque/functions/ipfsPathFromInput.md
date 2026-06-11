# Function: ipfsPathFromInput()

> **ipfsPathFromInput**(`input`): `string` \| `null`

Defined in: [packages/opaque/src/resolve.ts:112](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/resolve.ts#L112)

Extract the `<cid>[/path]` from an `ipfs://` URI, an `/ipfs/` gateway path, or a
bare CID (v0 `Qm…` base58 or v1 base32). Returns `null` when the input is not IPFS-shaped.

## Parameters

### input

`string`

## Returns

`string` \| `null`
