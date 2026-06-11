# Interface: ResolveRecipientMetaResult

Defined in: [packages/opaque/src/client.ts:503](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L503)

Result of [OpaqueClient.resolveRecipientMetaAddress](../classes/OpaqueClient.md#resolverecipientmetaaddress): registry lookup for a normal EOA.

## Properties

### metaAddressHex?

> `optional` **metaAddressHex?**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:515](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L515)

66-byte stealth meta-address (`0x` + 132 hex) for prepareStealthSend.
Omitted when `registered` is false.

***

### recipientAddress

> **recipientAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:508](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L508)

Checksummed address you looked up (the would-be recipient).
When `registered` is false, use this as the plain receiver identity — there is no meta-address yet.

***

### registered

> **registered**: `boolean`

Defined in: [packages/opaque/src/client.ts:510](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L510)

True when `stealthMetaAddressOf` returned a 66-byte meta-address for EIP-5564 scheme 1.
