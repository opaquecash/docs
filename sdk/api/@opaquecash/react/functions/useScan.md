# Function: useScan()

> **useScan**(`options?`): [`UseScanResult`](/sdk/api/@opaquecash/react/interfaces/UseScanResult.md)

Defined in: [useScan.ts:40](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/react/src/useScan.ts#L40)

Scan the unified cross-chain inbox for outputs owned by the provided client's wallet.
Scans once on mount (and whenever the client or options change); set `pollInterval`
to keep it fresh. Returns empty state with `loading: false` while the client is null.

## Parameters

### options?

[`UseScanOptions`](/sdk/api/@opaquecash/react/interfaces/UseScanOptions.md) = `{}`

## Returns

[`UseScanResult`](/sdk/api/@opaquecash/react/interfaces/UseScanResult.md)
