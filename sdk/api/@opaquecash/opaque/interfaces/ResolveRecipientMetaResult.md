# Interface: ResolveRecipientMetaResult

Defined in: [packages/opaque/src/client.ts:683](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L683)

Result of [OpaqueClient.resolveRecipientMetaAddress](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#resolverecipientmetaaddress): registry lookup for a normal EOA.

## Properties

### metaAddressHex?

> `optional` **metaAddressHex?**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:695](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L695)

66-byte stealth meta-address (`0x` + 132 hex) for prepareStealthSend.
Omitted when `registered` is false.

***

### recipientAddress

> **recipientAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:688](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L688)

Checksummed address you looked up (the would-be recipient).
When `registered` is false, use this as the plain receiver identity — there is no meta-address yet.

***

### registered

> **registered**: `boolean`

Defined in: [packages/opaque/src/client.ts:690](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L690)

True when `stealthMetaAddressOf` returned a 66-byte meta-address for EIP-5564 scheme 1.
