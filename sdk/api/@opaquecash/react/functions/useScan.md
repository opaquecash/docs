# Function: useScan()

> **useScan**(`options?`): [`UseScanResult`](/sdk/api/@opaquecash/react/interfaces/UseScanResult.md)

Defined in: [useScan.ts:40](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/react/src/useScan.ts#L40)

Scan the unified cross-chain inbox for outputs owned by the provided client's wallet.
Scans once on mount (and whenever the client or options change); set `pollInterval`
to keep it fresh. Returns empty state with `loading: false` while the client is null.

## Parameters

### options?

[`UseScanOptions`](/sdk/api/@opaquecash/react/interfaces/UseScanOptions.md) = `{}`

## Returns

[`UseScanResult`](/sdk/api/@opaquecash/react/interfaces/UseScanResult.md)
