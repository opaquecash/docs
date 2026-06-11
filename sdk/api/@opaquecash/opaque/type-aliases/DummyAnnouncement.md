# Type Alias: DummyAnnouncement

> **DummyAnnouncement** = [`PrepareStealthSendResult`](../interfaces/PrepareStealthSendResult.md) & `object`

Defined in: [packages/opaque/src/client.ts:492](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L492)

One decoy announcement from [OpaqueClient.generateDummyAnnouncements](../classes/OpaqueClient.md#generatedummyannouncements): a valid
DKSAP derivation against a throwaway meta-address (included for inspection; its
private keys are already gone).

## Type Declaration

### metaAddressHex

> **metaAddressHex**: `Hex`
