# Function: OpaqueProvider()

> **OpaqueProvider**(`props`): `FunctionComponentElement`\<`ProviderProps`\<[`OpaqueClient`](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md) \| `null`\>\>

Defined in: [context.ts:18](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/react/src/context.ts#L18)

Provide one `OpaqueClient` to the tree. Construct it with `OpaqueClient.fromWallet`
(one unified-signer shape per chain) and rebuild it when the connected wallets change;
the hooks below re-run automatically because the context value is the client instance.

## Parameters

### props

[`OpaqueProviderProps`](/sdk/api/@opaquecash/react/interfaces/OpaqueProviderProps.md)

## Returns

`FunctionComponentElement`\<`ProviderProps`\<[`OpaqueClient`](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md) \| `null`\>\>
