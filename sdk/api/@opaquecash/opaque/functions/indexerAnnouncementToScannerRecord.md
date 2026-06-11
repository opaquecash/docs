# Function: indexerAnnouncementToScannerRecord()

> **indexerAnnouncementToScannerRecord**(`row`): `AnnouncementJsonRecord`

Defined in: [packages/opaque/src/indexer/normalize.ts:12](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/indexer/normalize.ts#L12)

Map a subgraph/indexer row into the JSON record expected by `scan_attestations_wasm`.

## Parameters

### row

[`IndexerAnnouncement`](../interfaces/IndexerAnnouncement.md)

## Returns

`AnnouncementJsonRecord`
