# Interface: RegisterMetaAddressResult

Defined in: [packages/opaque/src/client.ts:491](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L491)

Result of [OpaqueClient.registerMetaAddress](../classes/OpaqueClient.md#registermetaaddress).

## Properties

### chain

> **chain**: [`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:493](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L493)

Chain the meta-address was registered on.

***

### metaAddressHex

> **metaAddressHex**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:497](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L497)

The 66-byte meta-address that was registered.

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:495](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L495)

EVM `0x` tx hash or Solana base58 signature.
