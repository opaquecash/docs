# Function: OpaqueProvider()

> **OpaqueProvider**(`props`): `FunctionComponentElement`\<`ProviderProps`\<[`OpaqueClient`](../../opaque/classes/OpaqueClient.md) \| `null`\>\>

Defined in: [context.ts:18](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/react/src/context.ts#L18)

Provide one `OpaqueClient` to the tree. Construct it with `OpaqueClient.fromWallet`
(one unified-signer shape per chain) and rebuild it when the connected wallets change;
the hooks below re-run automatically because the context value is the client instance.

## Parameters

### props

[`OpaqueProviderProps`](../interfaces/OpaqueProviderProps.md)

## Returns

`FunctionComponentElement`\<`ProviderProps`\<[`OpaqueClient`](../../opaque/classes/OpaqueClient.md) \| `null`\>\>
