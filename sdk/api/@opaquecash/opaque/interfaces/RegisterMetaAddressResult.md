# Interface: RegisterMetaAddressResult

Defined in: [packages/opaque/src/client.ts:520](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L520)

Result of [OpaqueClient.registerMetaAddress](../classes/OpaqueClient.md#registermetaaddress).

## Properties

### chain

> **chain**: [`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:522](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L522)

Chain the meta-address was registered on.

***

### metaAddressHex

> **metaAddressHex**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:526](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L526)

The 66-byte meta-address that was registered.

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:524](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L524)

EVM `0x` tx hash or Solana base58 signature.
