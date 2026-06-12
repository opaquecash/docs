# Function: indexerAnnouncementToScannerRecord()

> **indexerAnnouncementToScannerRecord**(`row`): `AnnouncementJsonRecord`

Defined in: [packages/opaque/src/indexer/normalize.ts:12](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/indexer/normalize.ts#L12)

Map a subgraph/indexer row into the JSON record expected by `scan_attestations_wasm`.

## Parameters

### row

[`IndexerAnnouncement`](/sdk/api/@opaquecash/opaque/interfaces/IndexerAnnouncement.md)

## Returns

`AnnouncementJsonRecord`
