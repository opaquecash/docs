# Function: isOnsNameInput()

> **isOnsNameInput**(`input`, `parentName`): `boolean`

Defined in: [packages/opaque/src/resolve.ts:124](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/resolve.ts#L124)

True when `input` is a depth-1 subname of the ONS parent in force
(`alice.opq.eth` for parent `opq.eth`; `alice.opqtest.eth` on testnet).

## Parameters

### input

`string`

### parentName

`string`

## Returns

`boolean`
