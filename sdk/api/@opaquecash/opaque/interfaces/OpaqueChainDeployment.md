# Interface: OpaqueChainDeployment

Defined in: [packages/opaque/src/chains.ts:16](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/chains.ts#L16)

Contract bundle for one chain (Opaque deployments).

## Properties

### chainId

> **chainId**: `number`

Defined in: [packages/opaque/src/chains.ts:17](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/chains.ts#L17)

***

### defaultTrackedTokens

> **defaultTrackedTokens**: `TrackedToken`[]

Defined in: [packages/opaque/src/chains.ts:26](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/chains.ts#L26)

Default tokens merged with `OpaqueClientConfig.trackedTokens`.

***

### name

> **name**: `string`

Defined in: [packages/opaque/src/chains.ts:18](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/chains.ts#L18)

***

### opaqueReputationVerifier?

> `optional` **opaqueReputationVerifier?**: `` `0x${string}` ``

Defined in: [packages/opaque/src/chains.ts:22](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/chains.ts#L22)

Optional PSR verifier; omitted if not deployed.

***

### stealthAddressAnnouncer

> **stealthAddressAnnouncer**: `` `0x${string}` ``

Defined in: [packages/opaque/src/chains.ts:20](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/chains.ts#L20)

***

### stealthMetaAddressRegistry

> **stealthMetaAddressRegistry**: `` `0x${string}` ``

Defined in: [packages/opaque/src/chains.ts:19](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/chains.ts#L19)

***

### stealthTokenSweep?

> `optional` **stealthTokenSweep?**: `` `0x${string}` ``

Defined in: [packages/opaque/src/chains.ts:24](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/chains.ts#L24)

Optional gasless ERC-20 sweep forwarder; omitted if not deployed.
