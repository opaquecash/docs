# Interface: TokenBalanceSummary

Defined in: [packages/opaque/src/types/indexer.ts:38](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L38)

Aggregated balance for a single tracked asset across all owned stealth addresses.

## Properties

### decimals

> **decimals**: `number`

Defined in: [packages/opaque/src/types/indexer.ts:42](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L42)

***

### symbol

> **symbol**: `string`

Defined in: [packages/opaque/src/types/indexer.ts:41](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L41)

***

### tokenAddress

> **tokenAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/types/indexer.ts:40](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L40)

`0x0000…0000` denotes native ETH when using [NATIVE\_TOKEN\_ADDRESS](/sdk/api/@opaquecash/opaque/variables/NATIVE_TOKEN_ADDRESS.md).

***

### totalRaw

> **totalRaw**: `bigint`

Defined in: [packages/opaque/src/types/indexer.ts:44](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/types/indexer.ts#L44)

Sum of raw units (wei for ETH, base units for ERC-20).
