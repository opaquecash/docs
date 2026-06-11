# Function: announcementToIndexerRow()

> **announcementToIndexerRow**(`a`): [`IndexerAnnouncement`](../interfaces/IndexerAnnouncement.md)

Defined in: [packages/opaque/src/client.ts:2653](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L2653)

Map a chain-neutral [Announcement](../interfaces/Announcement.md) (from any [ChainAdapter](../interfaces/ChainAdapter.md)) into the
[IndexerAnnouncement](../interfaces/IndexerAnnouncement.md) row shape consumed by [OpaqueClient.filterOwnedAnnouncements](../classes/OpaqueClient.md#filterownedannouncements).
`txHash` passes through verbatim (an EVM `0x` hash or a Solana base58 signature); `cursor`
(EVM block / Solana slot) becomes `blockNumber`.

## Parameters

### a

[`Announcement`](../interfaces/Announcement.md)

## Returns

[`IndexerAnnouncement`](../interfaces/IndexerAnnouncement.md)
