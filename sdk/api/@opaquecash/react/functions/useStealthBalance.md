# Function: useStealthBalance()

> **useStealthBalance**(`outputs`): [`UseStealthBalanceResult`](../interfaces/UseStealthBalanceResult.md)

Defined in: useStealthBalance.ts:21

Resolve the native balance of each owned stealth output (typically the `outputs`
from [useScan](useScan.md)). Refetches when the output set or client changes.

## Parameters

### outputs

[`UnifiedOwnedOutput`](../../opaque/interfaces/UnifiedOwnedOutput.md)[]

## Returns

[`UseStealthBalanceResult`](../interfaces/UseStealthBalanceResult.md)
