# Function: indexerAnnouncementToScannerRecord()

> **indexerAnnouncementToScannerRecord**(`row`): `AnnouncementJsonRecord`

Defined in: [packages/opaque/src/indexer/normalize.ts:12](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/indexer/normalize.ts#L12)

Map a subgraph/indexer row into the JSON record expected by `scan_attestations_wasm`.

## Parameters

### row

[`IndexerAnnouncement`](/sdk/api/@opaquecash/opaque/interfaces/IndexerAnnouncement.md)

## Returns

`AnnouncementJsonRecord`
