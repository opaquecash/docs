# Function: useScan()

> **useScan**(`options?`): [`UseScanResult`](../interfaces/UseScanResult.md)

Defined in: [useScan.ts:40](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/react/src/useScan.ts#L40)

Scan the unified cross-chain inbox for outputs owned by the provided client's wallet.
Scans once on mount (and whenever the client or options change); set `pollInterval`
to keep it fresh. Returns empty state with `loading: false` while the client is null.

## Parameters

### options?

[`UseScanOptions`](../interfaces/UseScanOptions.md) = `{}`

## Returns

[`UseScanResult`](../interfaces/UseScanResult.md)
