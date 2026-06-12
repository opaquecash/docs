# Function: externalNullifierFromScope()

> **externalNullifierFromScope**(`scope`): `bigint`

Defined in: packages/psr-core/dist/scope.d.ts:34

Map a scope string to a `uint256` external nullifier using Keccak-256 (left-padded to 32 bytes).

Must stay consistent with how your circuit expects the external nullifier input.

## Parameters

### scope

`string`

Output of [buildActionScope](/sdk/api/@opaquecash/opaque/functions/buildActionScope.md).

## Returns

`bigint`
