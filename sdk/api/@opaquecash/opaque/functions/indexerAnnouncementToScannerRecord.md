# Function: indexerAnnouncementToScannerRecord()

> **indexerAnnouncementToScannerRecord**(`row`): `AnnouncementJsonRecord`

Defined in: [packages/opaque/src/indexer/normalize.ts:12](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/indexer/normalize.ts#L12)

Map a subgraph/indexer row into the JSON record expected by `scan_attestations_wasm`.

## Parameters

### row

[`IndexerAnnouncement`](../interfaces/IndexerAnnouncement.md)

## Returns

`AnnouncementJsonRecord`
