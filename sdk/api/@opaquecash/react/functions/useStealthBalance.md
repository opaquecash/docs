# Function: useStealthBalance()

> **useStealthBalance**(`outputs`): [`UseStealthBalanceResult`](../interfaces/UseStealthBalanceResult.md)

Defined in: [useStealthBalance.ts:21](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/react/src/useStealthBalance.ts#L21)

Resolve the native balance of each owned stealth output (typically the `outputs`
from [useScan](useScan.md)). Refetches when the output set or client changes.

## Parameters

### outputs

[`UnifiedOwnedOutput`](../../opaque/interfaces/UnifiedOwnedOutput.md)[]

## Returns

[`UseStealthBalanceResult`](../interfaces/UseStealthBalanceResult.md)
