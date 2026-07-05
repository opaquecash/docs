# Function: resolveIpfsDidMetaAddress()

> **resolveIpfsDidMetaAddress**(`cidPath`, `transports?`): `Promise`\<`` `0x${string}` ``\>

Defined in: [packages/opaque/src/resolve.ts:220](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/resolve.ts#L220)

Fetch a DID document from IPFS via the configured gateways (tried in order) and
extract its meta-address. Throws when every gateway fails or no valid meta-address
is present in the document.

## Parameters

### cidPath

`string`

### transports?

[`ResolveTransports`](/sdk/api/@opaquecash/opaque/interfaces/ResolveTransports.md) = `{}`

## Returns

`Promise`\<`` `0x${string}` ``\>
