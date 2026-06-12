# Interface: FetchAnnouncementsOptions

Defined in: packages/adapter/dist/index.d.ts:48

Options for [ChainAdapter.fetchAnnouncements](/sdk/api/@opaquecash/opaque/interfaces/ChainAdapter.md#fetchannouncements).

## Properties

### fromCursor?

> `optional` **fromCursor?**: `bigint`

Defined in: packages/adapter/dist/index.d.ts:50

Inclusive lower bound cursor (EVM block number or Solana slot).

***

### includeCrossChain?

> `optional` **includeCrossChain?**: `boolean`

Defined in: packages/adapter/dist/index.d.ts:60

Also include cross-chain (UAB) announcements relayed TO this chain, normalised to the
same [Announcement](/sdk/api/@opaquecash/opaque/interfaces/Announcement.md) shape with their *origin* `chainId`. Adapter-interpreted:
defaults to `true` where the chain has a UAB receiver deployment configured.

***

### limit?

> `optional` **limit?**: `number`

Defined in: packages/adapter/dist/index.d.ts:54

Soft cap on the number of source records to scan (adapter-interpreted).

***

### toCursor?

> `optional` **toCursor?**: `bigint`

Defined in: packages/adapter/dist/index.d.ts:52

Inclusive upper bound cursor; omit for the chain tip.
