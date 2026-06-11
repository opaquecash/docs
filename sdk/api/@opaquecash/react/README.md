# @opaquecash/react

`@opaquecash/react` — React hooks for the Opaque SDK.

Wrap your tree in [OpaqueProvider](functions/OpaqueProvider.md) with a client built via
`OpaqueClient.fromWallet` (or `create`), then read it anywhere with
[useOpaqueClient](functions/useOpaqueClient.md), scan the unified inbox with [useScan](functions/useScan.md), and resolve
per-output native balances with [useStealthBalance](functions/useStealthBalance.md).

## Interfaces

- [OpaqueProviderProps](interfaces/OpaqueProviderProps.md)
- [UseScanOptions](interfaces/UseScanOptions.md)
- [UseScanResult](interfaces/UseScanResult.md)
- [UseStealthBalanceResult](interfaces/UseStealthBalanceResult.md)

## Functions

- [OpaqueProvider](functions/OpaqueProvider.md)
- [useOpaqueClient](functions/useOpaqueClient.md)
- [useOpaqueClientOrNull](functions/useOpaqueClientOrNull.md)
- [useScan](functions/useScan.md)
- [useStealthBalance](functions/useStealthBalance.md)
