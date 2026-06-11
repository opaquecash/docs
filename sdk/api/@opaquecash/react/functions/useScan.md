# Function: useScan()

> **useScan**(`options?`): [`UseScanResult`](../interfaces/UseScanResult.md)

Defined in: [useScan.ts:40](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/react/src/useScan.ts#L40)

Scan the unified cross-chain inbox for outputs owned by the provided client's wallet.
Scans once on mount (and whenever the client or options change); set `pollInterval`
to keep it fresh. Returns empty state with `loading: false` while the client is null.

## Parameters

### options?

[`UseScanOptions`](../interfaces/UseScanOptions.md) = `{}`

## Returns

[`UseScanResult`](../interfaces/UseScanResult.md)
