# Function: resolveSnsMetaAddress()

> **resolveSnsMetaAddress**(`name`, `snsGetRecord`): `Promise`\<`` `0x${string}` ``\>

Defined in: [packages/opaque/src/resolve.ts:137](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/resolve.ts#L137)

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
