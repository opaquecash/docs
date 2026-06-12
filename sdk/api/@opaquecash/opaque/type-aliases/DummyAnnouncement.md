# Type Alias: DummyAnnouncement

> **DummyAnnouncement** = [`PrepareStealthSendResult`](/sdk/api/@opaquecash/opaque/interfaces/PrepareStealthSendResult.md) & `object`

Defined in: [packages/opaque/src/client.ts:529](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L529)

One decoy announcement from [OpaqueClient.generateDummyAnnouncements](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#generatedummyannouncements): a valid
DKSAP derivation against a throwaway meta-address (included for inspection; its
private keys are already gone).

## Type Declaration

### metaAddressHex

> **metaAddressHex**: `Hex`
