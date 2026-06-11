# Interface: ResolveRecipientMetaResult

Defined in: [packages/opaque/src/client.ts:552](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L552)

Result of [OpaqueClient.resolveRecipientMetaAddress](../classes/OpaqueClient.md#resolverecipientmetaaddress): registry lookup for a normal EOA.

## Properties

### metaAddressHex?

> `optional` **metaAddressHex?**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:564](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L564)

66-byte stealth meta-address (`0x` + 132 hex) for prepareStealthSend.
Omitted when `registered` is false.

***

### recipientAddress

> **recipientAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:557](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L557)

Checksummed address you looked up (the would-be recipient).
When `registered` is false, use this as the plain receiver identity — there is no meta-address yet.

***

### registered

> **registered**: `boolean`

Defined in: [packages/opaque/src/client.ts:559](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L559)

True when `stealthMetaAddressOf` returned a 66-byte meta-address for EIP-5564 scheme 1.
