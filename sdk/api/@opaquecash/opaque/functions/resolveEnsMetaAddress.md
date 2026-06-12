# Function: resolveEnsMetaAddress()

> **resolveEnsMetaAddress**(`name`, `transports`): `Promise`\<`` `0x${string}` ``\>

Defined in: [packages/opaque/src/resolve.ts:263](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/resolve.ts#L263)

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
