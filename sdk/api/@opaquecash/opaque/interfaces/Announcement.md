# Interface: Announcement

Defined in: packages/adapter/dist/index.d.ts:29

A chain-neutral stealth announcement, as surfaced by a [ChainAdapter](ChainAdapter.md).

Mirrors `opaque_scanner::dksap::Announcement`. Each adapter decodes its chain's native
event/log into this shape so the cheap view-tag filter and the expensive DKSAP recovery
run once, regardless of source chain.

## Properties

### chainId

> **chainId**: `number`

Defined in: packages/adapter/dist/index.d.ts:39

Wormhole chain id of the source chain (Ethereum = 2, Solana = 1).

***

### cursor?

> `optional` **cursor?**: `bigint`

Defined in: packages/adapter/dist/index.d.ts:43

Source cursor: EVM block number or Solana slot, when known.

***

### ephemeralPubKey

> **ephemeralPubKey**: `Uint8Array`

Defined in: packages/adapter/dist/index.d.ts:33

Sender ephemeral public key: 33-byte compressed secp256k1.

***

### logIndex?

> `optional` **logIndex?**: `number`

Defined in: packages/adapter/dist/index.d.ts:45

Log index within the source transaction, when applicable (EVM).

***

### metadata

> **metadata**: `Uint8Array`

Defined in: packages/adapter/dist/index.d.ts:37

Raw announcement metadata (scheme-specific payload; `metadata[0]` is the view tag).

***

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

Defined in: packages/adapter/dist/index.d.ts:31

Scanner-matching id: 20-byte EVM-style stealth address, `0x`-prefixed lowercase hex.

***

### txHash?

> `optional` **txHash?**: `string`

Defined in: packages/adapter/dist/index.d.ts:41

Source transaction hash (EVM) or signature (Solana), when known.

***

### viewTag

> **viewTag**: `number`

Defined in: packages/adapter/dist/index.d.ts:35

View tag (`metadata[0]`) for the cheap pre-filter.
