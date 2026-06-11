# Function: extractMetaAddressFromDidDocument()

> **extractMetaAddressFromDidDocument**(`doc`): `` `0x${string}` `` \| `null`

Defined in: [packages/opaque/src/resolve.ts:139](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/resolve.ts#L139)

Pull a meta-address out of a DID document (or any JSON object) fetched from IPFS.
Accepted shapes, in order:
  1. a `service` entry of type `OpaqueStealthMetaAddress` whose `serviceEndpoint`
     carries the value (W3C DID style)
  2. a top-level `com.opaque.meta` or `opaqueMetaAddress` field
Values may be `st:opq:`-prefixed; both halves are point-validated.

## Parameters

### doc

`unknown`

## Returns

`` `0x${string}` `` \| `null`
