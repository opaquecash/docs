# Interface: UnifiedOwnedOutput

Defined in: [packages/opaque/src/client.ts:452](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L452)

One owned stealth output from the unified inbox, tagged with its source chain.

## Extends

- [`OwnedStealthOutput`](/sdk/api/@opaquecash/opaque/interfaces/OwnedStealthOutput.md)

## Properties

### attestationId?

> `optional` **attestationId?**: `number`

Defined in: [packages/opaque/src/types/indexer.ts:32](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/types/indexer.ts#L32)

Present when announcement carried PSR attestation metadata.

#### Inherited from

[`OwnedStealthOutput`](/sdk/api/@opaquecash/opaque/interfaces/OwnedStealthOutput.md).[`attestationId`](/sdk/api/@opaquecash/opaque/interfaces/OwnedStealthOutput.md#attestationid)

***

### blockNumber

> **blockNumber**: `number`

Defined in: [packages/opaque/src/types/indexer.ts:27](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/types/indexer.ts#L27)

#### Inherited from

[`OwnedStealthOutput`](/sdk/api/@opaquecash/opaque/interfaces/OwnedStealthOutput.md).[`blockNumber`](/sdk/api/@opaquecash/opaque/interfaces/OwnedStealthOutput.md#blocknumber)

***

### chain

> **chain**: [`OpaqueScanChain`](/sdk/api/@opaquecash/opaque/type-aliases/OpaqueScanChain.md)

Defined in: [packages/opaque/src/client.ts:454](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L454)

Source chain of this output.

***

### chainId

> **chainId**: `number`

Defined in: [packages/opaque/src/client.ts:456](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L456)

Wormhole chain id of the source (Ethereum = 2, Solana = 1).

***

### ephemeralPublicKey

> **ephemeralPublicKey**: `` `0x${string}` ``

Defined in: [packages/opaque/src/types/indexer.ts:30](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/types/indexer.ts#L30)

#### Inherited from

[`OwnedStealthOutput`](/sdk/api/@opaquecash/opaque/interfaces/OwnedStealthOutput.md).[`ephemeralPublicKey`](/sdk/api/@opaquecash/opaque/interfaces/OwnedStealthOutput.md#ephemeralpublickey)

***

### logIndex

> **logIndex**: `number`

Defined in: [packages/opaque/src/types/indexer.ts:28](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/types/indexer.ts#L28)

#### Inherited from

[`OwnedStealthOutput`](/sdk/api/@opaquecash/opaque/interfaces/OwnedStealthOutput.md).[`logIndex`](/sdk/api/@opaquecash/opaque/interfaces/OwnedStealthOutput.md#logindex)

***

### source

> **source**: `"native"` \| `"uab"`

Defined in: [packages/opaque/src/client.ts:461](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L461)

How the announcement was discovered: `"native"` (the chain's own announcer) or `"uab"`
(relayed cross-chain over Wormhole and re-emitted by the UABReceiver).

***

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/types/indexer.ts:25](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/types/indexer.ts#L25)

#### Inherited from

[`OwnedStealthOutput`](/sdk/api/@opaquecash/opaque/interfaces/OwnedStealthOutput.md).[`stealthAddress`](/sdk/api/@opaquecash/opaque/interfaces/OwnedStealthOutput.md#stealthaddress)

***

### transactionHash

> **transactionHash**: `` `0x${string}` ``

Defined in: [packages/opaque/src/types/indexer.ts:26](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/types/indexer.ts#L26)

#### Inherited from

[`OwnedStealthOutput`](/sdk/api/@opaquecash/opaque/interfaces/OwnedStealthOutput.md).[`transactionHash`](/sdk/api/@opaquecash/opaque/interfaces/OwnedStealthOutput.md#transactionhash)

***

### viewTag

> **viewTag**: `number`

Defined in: [packages/opaque/src/types/indexer.ts:29](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/types/indexer.ts#L29)

#### Inherited from

[`OwnedStealthOutput`](/sdk/api/@opaquecash/opaque/interfaces/OwnedStealthOutput.md).[`viewTag`](/sdk/api/@opaquecash/opaque/interfaces/OwnedStealthOutput.md#viewtag)
