# Interface: UseScanOptions

Defined in: [useScan.ts:6](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/react/src/useScan.ts#L6)

Options for [useScan](/sdk/api/@opaquecash/react/functions/useScan.md) (mirrors `OpaqueClient.scan`).

## Properties

### chains?

> `optional` **chains?**: [`OpaqueScanChain`](/sdk/api/@opaquecash/opaque/type-aliases/OpaqueScanChain.md)[]

Defined in: [useScan.ts:8](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/react/src/useScan.ts#L8)

Chains to scan (default both).

***

### fromBlock?

> `optional` **fromBlock?**: `bigint`

Defined in: [useScan.ts:10](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/react/src/useScan.ts#L10)

Lower-bound cursor: EVM block number (Solana scans the most recent signatures).

***

### includeCrossChain?

> `optional` **includeCrossChain?**: `boolean`

Defined in: [useScan.ts:16](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/react/src/useScan.ts#L16)

Merge cross-chain (UAB) announcements (adapter default when omitted).

***

### paused?

> `optional` **paused?**: `boolean`

Defined in: [useScan.ts:20](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/react/src/useScan.ts#L20)

Skip scanning while true (e.g. tab hidden).

***

### pollInterval?

> `optional` **pollInterval?**: `number`

Defined in: [useScan.ts:18](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/react/src/useScan.ts#L18)

Re-scan interval in ms; omit for scan-once (call `refresh` manually).

***

### solanaLimit?

> `optional` **solanaLimit?**: `number`

Defined in: [useScan.ts:14](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/react/src/useScan.ts#L14)

Max Solana signatures to scan (adapter default when omitted).

***

### toBlock?

> `optional` **toBlock?**: `bigint`

Defined in: [useScan.ts:12](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/react/src/useScan.ts#L12)

Upper-bound EVM block; omit for the chain tip.
