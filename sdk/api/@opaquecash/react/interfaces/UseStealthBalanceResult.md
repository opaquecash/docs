# Interface: UseStealthBalanceResult

Defined in: [useStealthBalance.ts:6](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/react/src/useStealthBalance.ts#L6)

State returned by [useStealthBalance](../functions/useStealthBalance.md).

## Properties

### balances

> **balances**: [`OutputBalance`](../../opaque/interfaces/OutputBalance.md)[]

Defined in: [useStealthBalance.ts:8](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/react/src/useStealthBalance.ts#L8)

Native balance per owned output (wei / lamports), in input order.

***

### error

> **error**: `Error` \| `null`

Defined in: [useStealthBalance.ts:14](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/react/src/useStealthBalance.ts#L14)

Last fetch error, cleared by the next successful fetch.

***

### loading

> **loading**: `boolean`

Defined in: [useStealthBalance.ts:12](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/react/src/useStealthBalance.ts#L12)

True while balances are being fetched.

***

### totals

> **totals**: `object`

Defined in: [useStealthBalance.ts:10](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/react/src/useStealthBalance.ts#L10)

Sum of `balances` per chain, in base units.

#### ethereum

> **ethereum**: `bigint`

#### solana

> **solana**: `bigint`
