# Interface: RegisterMetaAddressResult

Defined in: [packages/opaque/src/client.ts:671](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L671)

Result of [OpaqueClient.registerMetaAddress](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#registermetaaddress).

## Properties

### chain

> **chain**: [`OpaqueScanChain`](/sdk/api/@opaquecash/opaque/type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:673](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L673)

Chain the meta-address was registered on.

***

### metaAddressHex

> **metaAddressHex**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:677](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L677)

The 66-byte meta-address that was registered.

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:675](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L675)

EVM `0x` tx hash or Solana base58 signature.
