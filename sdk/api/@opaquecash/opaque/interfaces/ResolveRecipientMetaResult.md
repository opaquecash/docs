# Interface: ResolveRecipientMetaResult

Defined in: [packages/opaque/src/client.ts:569](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L569)

Result of [OpaqueClient.resolveRecipientMetaAddress](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#resolverecipientmetaaddress): registry lookup for a normal EOA.

## Properties

### metaAddressHex?

> `optional` **metaAddressHex?**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:581](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L581)

66-byte stealth meta-address (`0x` + 132 hex) for prepareStealthSend.
Omitted when `registered` is false.

***

### recipientAddress

> **recipientAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:574](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L574)

Checksummed address you looked up (the would-be recipient).
When `registered` is false, use this as the plain receiver identity — there is no meta-address yet.

***

### registered

> **registered**: `boolean`

Defined in: [packages/opaque/src/client.ts:576](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L576)

True when `stealthMetaAddressOf` returned a 66-byte meta-address for EIP-5564 scheme 1.
