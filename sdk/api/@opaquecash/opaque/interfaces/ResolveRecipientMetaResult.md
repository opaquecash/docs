# Interface: ResolveRecipientMetaResult

Defined in: [packages/opaque/src/client.ts:532](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L532)

Result of [OpaqueClient.resolveRecipientMetaAddress](../classes/OpaqueClient.md#resolverecipientmetaaddress): registry lookup for a normal EOA.

## Properties

### metaAddressHex?

> `optional` **metaAddressHex?**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:544](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L544)

66-byte stealth meta-address (`0x` + 132 hex) for prepareStealthSend.
Omitted when `registered` is false.

***

### recipientAddress

> **recipientAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:537](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L537)

Checksummed address you looked up (the would-be recipient).
When `registered` is false, use this as the plain receiver identity — there is no meta-address yet.

***

### registered

> **registered**: `boolean`

Defined in: [packages/opaque/src/client.ts:539](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L539)

True when `stealthMetaAddressOf` returned a 66-byte meta-address for EIP-5564 scheme 1.
