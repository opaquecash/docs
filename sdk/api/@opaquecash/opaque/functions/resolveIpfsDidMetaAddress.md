# Function: resolveIpfsDidMetaAddress()

> **resolveIpfsDidMetaAddress**(`cidPath`, `transports?`): `Promise`\<`` `0x${string}` ``\>

Defined in: [packages/opaque/src/resolve.ts:219](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/resolve.ts#L219)

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
