# Type Alias: DummyAnnouncement

> **DummyAnnouncement** = [`PrepareStealthSendResult`](/sdk/api/@opaquecash/opaque/interfaces/PrepareStealthSendResult.md) & `object`

Defined in: [packages/opaque/src/client.ts:643](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L643)

One decoy announcement from [OpaqueClient.generateDummyAnnouncements](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#generatedummyannouncements): a valid
DKSAP derivation against a throwaway meta-address (included for inspection; its
private keys are already gone).

## Type Declaration

### metaAddressHex

> **metaAddressHex**: `Hex`
