# Function: announcementToIndexerRow()

> **announcementToIndexerRow**(`a`): [`IndexerAnnouncement`](/sdk/api/@opaquecash/opaque/interfaces/IndexerAnnouncement.md)

Defined in: [packages/opaque/src/client.ts:3354](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L3354)

Map a chain-neutral [Announcement](/sdk/api/@opaquecash/opaque/interfaces/Announcement.md) (from any [ChainAdapter](/sdk/api/@opaquecash/opaque/interfaces/ChainAdapter.md)) into the
[IndexerAnnouncement](/sdk/api/@opaquecash/opaque/interfaces/IndexerAnnouncement.md) row shape consumed by [OpaqueClient.filterOwnedAnnouncements](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#filterownedannouncements).
`txHash` passes through verbatim (an EVM `0x` hash or a Solana base58 signature); `cursor`
(EVM block / Solana slot) becomes `blockNumber`.

## Parameters

### a

[`Announcement`](/sdk/api/@opaquecash/opaque/interfaces/Announcement.md)

## Returns

[`IndexerAnnouncement`](/sdk/api/@opaquecash/opaque/interfaces/IndexerAnnouncement.md)
