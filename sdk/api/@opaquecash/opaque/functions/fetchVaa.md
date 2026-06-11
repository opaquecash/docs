# Function: fetchVaa()

> **fetchVaa**(`whChain`, `emitterHex`, `sequence`, `opts?`): `Promise`\<`Uint8Array`\>

Defined in: packages/uab/dist/vaa.d.ts:13

Poll Wormholescan for the signed VAA of a published message.
`emitterHex` is the 32-byte Wormhole emitter address (with or without `0x`).

## Parameters

### whChain

`number`

### emitterHex

`string`

### sequence

`bigint`

### opts?

`FetchVaaOptions`

## Returns

`Promise`\<`Uint8Array`\>
