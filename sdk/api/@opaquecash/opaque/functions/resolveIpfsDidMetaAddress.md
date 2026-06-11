# Function: resolveIpfsDidMetaAddress()

> **resolveIpfsDidMetaAddress**(`cidPath`, `transports?`): `Promise`\<`` `0x${string}` ``\>

Defined in: [packages/opaque/src/resolve.ts:219](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/resolve.ts#L219)

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
