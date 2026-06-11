# Interface: UseScanResult

Defined in: [useScan.ts:24](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/react/src/useScan.ts#L24)

State returned by [useScan](../functions/useScan.md).

## Properties

### error

> **error**: `Error` \| `null`

Defined in: [useScan.ts:30](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/react/src/useScan.ts#L30)

Last scan error, cleared by the next successful scan.

***

### loading

> **loading**: `boolean`

Defined in: [useScan.ts:28](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/react/src/useScan.ts#L28)

True while a scan is in flight.

***

### outputs

> **outputs**: [`UnifiedOwnedOutput`](../../opaque/interfaces/UnifiedOwnedOutput.md)[]

Defined in: [useScan.ts:26](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/react/src/useScan.ts#L26)

Owned outputs from the unified inbox (empty while loading the first scan).

***

### refresh

> **refresh**: () => `void`

Defined in: [useScan.ts:32](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/react/src/useScan.ts#L32)

Trigger a re-scan now.

#### Returns

`void`
