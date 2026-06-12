# Interface: RegisterMetaAddressResult

Defined in: [packages/opaque/src/client.ts:557](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L557)

Result of [OpaqueClient.registerMetaAddress](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#registermetaaddress).

## Properties

### chain

> **chain**: [`OpaqueScanChain`](/sdk/api/@opaquecash/opaque/type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:559](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L559)

Chain the meta-address was registered on.

***

### metaAddressHex

> **metaAddressHex**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:563](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L563)

The 66-byte meta-address that was registered.

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:561](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L561)

EVM `0x` tx hash or Solana base58 signature.
