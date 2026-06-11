# Interface: RegisterMetaAddressResult

Defined in: [packages/opaque/src/client.ts:540](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L540)

Result of [OpaqueClient.registerMetaAddress](../classes/OpaqueClient.md#registermetaaddress).

## Properties

### chain

> **chain**: [`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:542](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L542)

Chain the meta-address was registered on.

***

### metaAddressHex

> **metaAddressHex**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:546](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L546)

The 66-byte meta-address that was registered.

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:544](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L544)

EVM `0x` tx hash or Solana base58 signature.
