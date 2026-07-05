# Interface: UseScanResult

Defined in: [useScan.ts:24](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/react/src/useScan.ts#L24)

State returned by [useScan](/sdk/api/@opaquecash/react/functions/useScan.md).

## Properties

### error

> **error**: `Error` \| `null`

Defined in: [useScan.ts:30](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/react/src/useScan.ts#L30)

Last scan error, cleared by the next successful scan.

***

### loading

> **loading**: `boolean`

Defined in: [useScan.ts:28](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/react/src/useScan.ts#L28)

True while a scan is in flight.

***

### outputs

> **outputs**: [`UnifiedOwnedOutput`](/sdk/api/@opaquecash/opaque/interfaces/UnifiedOwnedOutput.md)[]

Defined in: [useScan.ts:26](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/react/src/useScan.ts#L26)

Owned outputs from the unified inbox (empty while loading the first scan).

***

### refresh

> **refresh**: () => `void`

Defined in: [useScan.ts:32](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/react/src/useScan.ts#L32)

Trigger a re-scan now.

#### Returns

`void`
