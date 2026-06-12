# Function: resolveSnsMetaAddress()

> **resolveSnsMetaAddress**(`name`, `snsGetRecord`): `Promise`\<`` `0x${string}` ``\>

Defined in: [packages/opaque/src/resolve.ts:136](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/resolve.ts#L136)

Read the `com.opaque.meta` TXT record of a `.sol` domain through the injected
SNS reader and validate it. Throws when no reader is configured, the record is
unset, or the value is not a valid meta-address.

## Parameters

### name

`string`

### snsGetRecord

((`domain`, `key`) => `Promise`\<`string` \| `null`\>) \| `undefined`

## Returns

`Promise`\<`` `0x${string}` ``\>
