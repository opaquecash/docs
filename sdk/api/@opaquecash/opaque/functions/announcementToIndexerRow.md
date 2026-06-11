# Function: announcementToIndexerRow()

> **announcementToIndexerRow**(`a`): [`IndexerAnnouncement`](../interfaces/IndexerAnnouncement.md)

Defined in: [packages/opaque/src/client.ts:2376](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L2376)

Map a chain-neutral [Announcement](../interfaces/Announcement.md) (from any [ChainAdapter](../interfaces/ChainAdapter.md)) into the
[IndexerAnnouncement](../interfaces/IndexerAnnouncement.md) row shape consumed by [OpaqueClient.filterOwnedAnnouncements](../classes/OpaqueClient.md#filterownedannouncements).
`txHash` passes through verbatim (an EVM `0x` hash or a Solana base58 signature); `cursor`
(EVM block / Solana slot) becomes `blockNumber`.

## Parameters

### a

[`Announcement`](../interfaces/Announcement.md)

## Returns

[`IndexerAnnouncement`](../interfaces/IndexerAnnouncement.md)
