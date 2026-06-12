# Interface: IndexerAnnouncement

Defined in: [packages/opaque/src/types/indexer.ts:9](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L9)

Announcement row shape from a typical Graph subgraph (field names preserved).

`etherealPublicKey` is the **ephemeral** secp256k1 public key (33-byte compressed hex),
as commonly returned by indexers despite the name.

## Properties

### \_\_typename?

> `optional` **\_\_typename?**: `string`

Defined in: [packages/opaque/src/types/indexer.ts:10](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L10)

***

### blockNumber

> **blockNumber**: `string`

Defined in: [packages/opaque/src/types/indexer.ts:12](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L12)

***

### etherealPublicKey

> **etherealPublicKey**: `` `0x${string}` ``

Defined in: [packages/opaque/src/types/indexer.ts:13](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L13)

***

### id?

> `optional` **id?**: `string`

Defined in: [packages/opaque/src/types/indexer.ts:11](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L11)

***

### logIndex

> **logIndex**: `number`

Defined in: [packages/opaque/src/types/indexer.ts:14](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L14)

***

### metadata

> **metadata**: `` `0x${string}` ``

Defined in: [packages/opaque/src/types/indexer.ts:15](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L15)

***

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/types/indexer.ts:16](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L16)

***

### transactionHash

> **transactionHash**: `` `0x${string}` ``

Defined in: [packages/opaque/src/types/indexer.ts:17](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L17)

***

### viewTag

> **viewTag**: `number`

Defined in: [packages/opaque/src/types/indexer.ts:18](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L18)
