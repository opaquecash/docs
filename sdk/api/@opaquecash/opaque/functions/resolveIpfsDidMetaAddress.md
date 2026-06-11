# Function: resolveIpfsDidMetaAddress()

> **resolveIpfsDidMetaAddress**(`cidPath`, `transports?`): `Promise`\<`` `0x${string}` ``\>

Defined in: [packages/opaque/src/resolve.ts:168](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/resolve.ts#L168)

Fetch a DID document from IPFS via the configured gateways (tried in order) and
extract its meta-address. Throws when every gateway fails or no valid meta-address
is present in the document.

## Parameters

### cidPath

`string`

### transports?

[`ResolveTransports`](../interfaces/ResolveTransports.md) = `{}`

## Returns

`Promise`\<`` `0x${string}` ``\>
