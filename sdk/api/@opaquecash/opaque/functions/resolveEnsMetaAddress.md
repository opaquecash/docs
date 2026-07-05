# Function: resolveEnsMetaAddress()

> **resolveEnsMetaAddress**(`name`, `transports`): `Promise`\<`` `0x${string}` ``\>

Defined in: [packages/opaque/src/resolve.ts:264](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/resolve.ts#L264)

Read the `com.opaque.meta` text record for an ENS name through the injected reader
and validate it. Throws when the record is unset or invalid. The on-chain registry
stays authoritative on conflict (CSAP §2.9) — callers who also hold a registry entry
for the name's address SHOULD prefer that entry.

## Parameters

### name

`string`

### transports

[`ResolveTransports`](/sdk/api/@opaquecash/opaque/interfaces/ResolveTransports.md)

## Returns

`Promise`\<`` `0x${string}` ``\>
