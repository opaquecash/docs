# Function: OpaqueProvider()

> **OpaqueProvider**(`props`): `FunctionComponentElement`\<`ProviderProps`\<[`OpaqueClient`](../../opaque/classes/OpaqueClient.md) \| `null`\>\>

Defined in: context.ts:18

Provide one `OpaqueClient` to the tree. Construct it with `OpaqueClient.fromWallet`
(one unified-signer shape per chain) and rebuild it when the connected wallets change;
the hooks below re-run automatically because the context value is the client instance.

## Parameters

### props

[`OpaqueProviderProps`](../interfaces/OpaqueProviderProps.md)

## Returns

`FunctionComponentElement`\<`ProviderProps`\<[`OpaqueClient`](../../opaque/classes/OpaqueClient.md) \| `null`\>\>
