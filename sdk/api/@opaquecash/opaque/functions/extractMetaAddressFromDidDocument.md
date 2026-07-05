# Function: extractMetaAddressFromDidDocument()

> **extractMetaAddressFromDidDocument**(`doc`): `` `0x${string}` `` \| `null`

Defined in: [packages/opaque/src/resolve.ts:191](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/resolve.ts#L191)

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
