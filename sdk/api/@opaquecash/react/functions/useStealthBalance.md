# Function: useStealthBalance()

> **useStealthBalance**(`outputs`): [`UseStealthBalanceResult`](/sdk/api/@opaquecash/react/interfaces/UseStealthBalanceResult.md)

Defined in: [useStealthBalance.ts:21](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/react/src/useStealthBalance.ts#L21)

Resolve the native balance of each owned stealth output (typically the `outputs`
from [useScan](/sdk/api/@opaquecash/react/functions/useScan.md)). Refetches when the output set or client changes.

## Parameters

### outputs

[`UnifiedOwnedOutput`](/sdk/api/@opaquecash/opaque/interfaces/UnifiedOwnedOutput.md)[]

## Returns

[`UseStealthBalanceResult`](/sdk/api/@opaquecash/react/interfaces/UseStealthBalanceResult.md)
