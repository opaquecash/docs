# Interface: OwnedStealthOutput

Defined in: [packages/opaque/src/types/indexer.ts:24](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L24)

One output the recipient owns (from WASM `scan_attestations` + normalized context).

## Extended by

- [`UnifiedOwnedOutput`](/sdk/api/@opaquecash/opaque/interfaces/UnifiedOwnedOutput.md)

## Properties

### attestationId?

> `optional` **attestationId?**: `number`

Defined in: [packages/opaque/src/types/indexer.ts:32](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L32)

Present when announcement carried PSR attestation metadata.

***

### blockNumber

> **blockNumber**: `number`

Defined in: [packages/opaque/src/types/indexer.ts:27](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L27)

***

### ephemeralPublicKey

> **ephemeralPublicKey**: `` `0x${string}` ``

Defined in: [packages/opaque/src/types/indexer.ts:30](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L30)

***

### logIndex

> **logIndex**: `number`

Defined in: [packages/opaque/src/types/indexer.ts:28](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L28)

***

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/types/indexer.ts:25](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L25)

***

### transactionHash

> **transactionHash**: `` `0x${string}` ``

Defined in: [packages/opaque/src/types/indexer.ts:26](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L26)

***

### viewTag

> **viewTag**: `number`

Defined in: [packages/opaque/src/types/indexer.ts:29](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L29)
