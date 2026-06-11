# Type Alias: DummyAnnouncement

> **DummyAnnouncement** = [`PrepareStealthSendResult`](../interfaces/PrepareStealthSendResult.md) & `object`

Defined in: [packages/opaque/src/client.ts:463](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L463)

One decoy announcement from [OpaqueClient.generateDummyAnnouncements](../classes/OpaqueClient.md#generatedummyannouncements): a valid
DKSAP derivation against a throwaway meta-address (included for inspection; its
private keys are already gone).

## Type Declaration

### metaAddressHex

> **metaAddressHex**: `Hex`
