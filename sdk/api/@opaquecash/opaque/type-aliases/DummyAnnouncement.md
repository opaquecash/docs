# Type Alias: DummyAnnouncement

> **DummyAnnouncement** = [`PrepareStealthSendResult`](../interfaces/PrepareStealthSendResult.md) & `object`

Defined in: [packages/opaque/src/client.ts:512](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L512)

One decoy announcement from [OpaqueClient.generateDummyAnnouncements](../classes/OpaqueClient.md#generatedummyannouncements): a valid
DKSAP derivation against a throwaway meta-address (included for inspection; its
private keys are already gone).

## Type Declaration

### metaAddressHex

> **metaAddressHex**: `Hex`
