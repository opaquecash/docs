# Function: indexerAnnouncementToScannerRecord()

> **indexerAnnouncementToScannerRecord**(`row`): `AnnouncementJsonRecord`

Defined in: [packages/opaque/src/indexer/normalize.ts:12](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/indexer/normalize.ts#L12)

Map a subgraph/indexer row into the JSON record expected by `scan_attestations_wasm`.

## Parameters

### row

[`IndexerAnnouncement`](../interfaces/IndexerAnnouncement.md)

## Returns

`AnnouncementJsonRecord`
