# Function: isOnsNameInput()

> **isOnsNameInput**(`input`, `parentName`): `boolean`

Defined in: [packages/opaque/src/resolve.ts:123](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/resolve.ts#L123)

True when `input` is a depth-1 subname of the ONS parent in force
(`alice.opq.eth` for parent `opq.eth`; `alice.opqtest.eth` on testnet).

## Parameters

### input

`string`

### parentName

`string`

## Returns

`boolean`
