# Interface: UseScanResult

Defined in: useScan.ts:24

State returned by [useScan](../functions/useScan.md).

## Properties

### error

> **error**: `Error` \| `null`

Defined in: useScan.ts:30

Last scan error, cleared by the next successful scan.

***

### loading

> **loading**: `boolean`

Defined in: useScan.ts:28

True while a scan is in flight.

***

### outputs

> **outputs**: [`UnifiedOwnedOutput`](../../opaque/interfaces/UnifiedOwnedOutput.md)[]

Defined in: useScan.ts:26

Owned outputs from the unified inbox (empty while loading the first scan).

***

### refresh

> **refresh**: () => `void`

Defined in: useScan.ts:32

Trigger a re-scan now.

#### Returns

`void`
