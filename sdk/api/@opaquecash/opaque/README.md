# @opaquecash/opaque

Single entry point for Opaque **stealth** (EIP-5564) and **PSR** flows used together with your own indexer.

**Full documentation** (guides, API reference, playground): **[docs.opaque.cash](https://docs.opaque.cash)**

## Install

```bash
npm install @opaquecash/opaque
```

The package ships TypeScript types and depends on **`viem`** (v2). You must load the **WASM** bundle (`cryptography.js`) at runtime—either from your app’s static assets or a hosted URL (see below).

### Working from this repository

```bash
cd sdk && npm install && npm run build
```

Then depend on `@opaquecash/opaque` via your workspace or `npm link`.

## Initialize

```ts
import { OpaqueClient } from "@opaquecash/opaque";

const client = await OpaqueClient.create({
  chainId: 11155111,
  rpcUrl: "https://…",
  walletSignature: userSignatureHex,
  ethereumAddress: userAddress,
  wasmModuleSpecifier: new URL("/pkg/cryptography.js", import.meta.url).href,
});
```

Hosted WASM entry used by the reference app:

`https://www.opaque.cash/pkg/cryptography.js`

## Constants

- `OpaqueClient.supportedChainIds()`
- `OpaqueClient.chainDeployment(chainId)` — registry, announcer, verifier, default tokens
- `NATIVE_TOKEN_ADDRESS` — sentinel for ETH in balance aggregation

## Indexer announcements

Pass subgraph-shaped rows:

```ts
const rows: IndexerAnnouncement[] = [
  {
    blockNumber: "10533630",
    etherealPublicKey: "0x02…",
    logIndex: 161,
    metadata: "0x…",
    stealthAddress: "0x…",
    transactionHash: "0x…",
    viewTag: 234,
  },
];
```

## Flows

| Goal | API |
|------|-----|
| Resolve recipient meta-address (registry read via `rpcUrl`) | `resolveRecipientMetaAddress(normalAddress)` |
| Register meta-address calldata | `buildRegisterMetaAddressTransaction()` |
| Send: derive stealth + ephemeral | `prepareStealthSend(recipientMetaHex)` |
| Announce calldata | `buildAnnounceTransactionRequest(prepareResult)` |
| Owned outputs | `filterOwnedAnnouncements(rows)` |
| Balances by token | `getBalancesFromAnnouncements(rows)` |
| PSR traits | `discoverTraits(rows)` |

You always submit transactions from your own wallet; the SDK returns **structured calldata** and **read results**.

## Lower-level packages

`@opaquecash/stealth-core`, `@opaquecash/stealth-wasm`, `@opaquecash/stealth-chain`, `@opaquecash/psr-core`, and related packages remain available for advanced integrations.

`@opaquecash/opaque` — unified Opaque SDK client.

Initialize once with chain, RPC, wallet signature, and WASM URL; then prepare txs,
filter indexer announcements, aggregate balances, reconstruct one-time spend keys, and discover PSR traits.

## Namespaces

- [solanaPsr](namespaces/solanaPsr/README.md)

## Classes

- [EvmAdapter](classes/EvmAdapter.md)
- [OpaqueClient](classes/OpaqueClient.md)
- [SolanaAdapter](classes/SolanaAdapter.md)

## Interfaces

- [Announcement](interfaces/Announcement.md)
- [AnnouncementHandlers](interfaces/AnnouncementHandlers.md)
- [AnnounceTransactionRequest](interfaces/AnnounceTransactionRequest.md)
- [AnnounceWithRelayRequest](interfaces/AnnounceWithRelayRequest.md)
- [ArtifactPaths](interfaces/ArtifactPaths.md)
- [AttestationV2](interfaces/AttestationV2.md)
- [ChainAdapter](interfaces/ChainAdapter.md)
- [CreateSchemaParams](interfaces/CreateSchemaParams.md)
- [CreateSchemaResult](interfaces/CreateSchemaResult.md)
- [CrossChainAnnouncementRecord](interfaces/CrossChainAnnouncementRecord.md)
- [DiscoveredTrait](interfaces/DiscoveredTrait.md)
- [EvmAdapterConfig](interfaces/EvmAdapterConfig.md)
- [EvmAnnounceWithRelayResult](interfaces/EvmAnnounceWithRelayResult.md)
- [EvmUnifiedSigner](interfaces/EvmUnifiedSigner.md)
- [FetchAnnouncementsOptions](interfaces/FetchAnnouncementsOptions.md)
- [FieldDef](interfaces/FieldDef.md)
- [IndexerAnnouncement](interfaces/IndexerAnnouncement.md)
- [IssueAttestationParams](interfaces/IssueAttestationParams.md)
- [IssueAttestationResult](interfaces/IssueAttestationResult.md)
- [OpaqueChainDeployment](interfaces/OpaqueChainDeployment.md)
- [OpaqueClientConfig](interfaces/OpaqueClientConfig.md)
- [OutputBalance](interfaces/OutputBalance.md)
- [OwnedStealthOutput](interfaces/OwnedStealthOutput.md)
- [PrepareStealthSendResult](interfaces/PrepareStealthSendResult.md)
- [ProofData](interfaces/ProofData.md)
- [PsrExpiryInput](interfaces/PsrExpiryInput.md)
- [PsrTxResult](interfaces/PsrTxResult.md)
- [RegisterMetaAddressResult](interfaces/RegisterMetaAddressResult.md)
- [RegisterMetaAddressTransactionRequest](interfaces/RegisterMetaAddressTransactionRequest.md)
- [ResolvedRecipient](interfaces/ResolvedRecipient.md)
- [ResolveRecipientMetaResult](interfaces/ResolveRecipientMetaResult.md)
- [ResolveTransports](interfaces/ResolveTransports.md)
- [SchemaV2](interfaces/SchemaV2.md)
- [SendStealthPaymentParams](interfaces/SendStealthPaymentParams.md)
- [SendStealthPaymentResult](interfaces/SendStealthPaymentResult.md)
- [SolanaAdapterConfig](interfaces/SolanaAdapterConfig.md)
- [SolanaAnnounceWithRelayResult](interfaces/SolanaAnnounceWithRelayResult.md)
- [SolanaDeployment](interfaces/SolanaDeployment.md)
- [SolanaUnifiedSigner](interfaces/SolanaUnifiedSigner.md)
- [TokenBalanceSummary](interfaces/TokenBalanceSummary.md)
- [UabDeployment](interfaces/UabDeployment.md)
- [UabIndexerAnnouncement](interfaces/UabIndexerAnnouncement.md)
- [UabPayload](interfaces/UabPayload.md)
- [UnifiedOwnedOutput](interfaces/UnifiedOwnedOutput.md)
- [VerifyReputationArgs](interfaces/VerifyReputationArgs.md)

## Type Aliases

- [AnnounceWithRelayResult](type-aliases/AnnounceWithRelayResult.md)
- [AttestationField](type-aliases/AttestationField.md)
- [DummyAnnouncement](type-aliases/DummyAnnouncement.md)
- [FieldType](type-aliases/FieldType.md)
- [OpaqueScanChain](type-aliases/OpaqueScanChain.md)
- [PrepareGhostReceiveResult](type-aliases/PrepareGhostReceiveResult.md)
- [ProofProgressCallback](type-aliases/ProofProgressCallback.md)
- [PsrChain](type-aliases/PsrChain.md)
- [ResolvedRecipientSource](type-aliases/ResolvedRecipientSource.md)
- [SolanaCluster](type-aliases/SolanaCluster.md)
- [UnifiedSigner](type-aliases/UnifiedSigner.md)

## Variables

- [CONSISTENCY\_FINALIZED](variables/CONSISTENCY_FINALIZED.md)
- [CONSISTENCY\_SAFE](variables/CONSISTENCY_SAFE.md)
- [DEFAULT\_IPFS\_GATEWAYS](variables/DEFAULT_IPFS_GATEWAYS.md)
- [DEFAULT\_REPUTATION\_ARTIFACT\_PATHS](variables/DEFAULT_REPUTATION_ARTIFACT_PATHS.md)
- [DEFAULT\_REPUTATION\_ARTIFACTS\_ORIGIN](variables/DEFAULT_REPUTATION_ARTIFACTS_ORIGIN.md)
- [EIP5564\_SCHEME\_SECP256K1](variables/EIP5564_SCHEME_SECP256K1.md)
- [META\_ADDRESS\_VALUE\_PREFIX](variables/META_ADDRESS_VALUE_PREFIX.md)
- [NATIVE\_TOKEN\_ADDRESS](variables/NATIVE_TOKEN_ADDRESS.md)
- [OPAQUE\_META\_RECORD\_KEY](variables/OPAQUE_META_RECORD_KEY.md)
- [SCHEMA\_VERSION](variables/SCHEMA_VERSION.md)
- [SETUP\_MESSAGE](variables/SETUP_MESSAGE.md)
- [UAB\_PAYLOAD\_LENGTH](variables/UAB_PAYLOAD_LENGTH.md)
- [WORMHOLE\_CHAIN\_ETHEREUM](variables/WORMHOLE_CHAIN_ETHEREUM.md)
- [WORMHOLE\_CHAIN\_ID](variables/WORMHOLE_CHAIN_ID.md)
- [WORMHOLE\_CHAIN\_SOLANA](variables/WORMHOLE_CHAIN_SOLANA.md)
- [WORMHOLESCAN\_MAINNET](variables/WORMHOLESCAN_MAINNET.md)
- [WORMHOLESCAN\_TESTNET](variables/WORMHOLESCAN_TESTNET.md)
- [ZERO\_ADDRESS](variables/ZERO_ADDRESS.md)
- [ZERO\_BYTES32](variables/ZERO_BYTES32.md)

## Functions

- [announcementToIndexerRow](functions/announcementToIndexerRow.md)
- [buildActionScope](functions/buildActionScope.md)
- [computeSchemaId](functions/computeSchemaId.md)
- [computeStealthAddressAndViewTag](functions/computeStealthAddressAndViewTag.md)
- [computeUid](functions/computeUid.md)
- [decodeAttestationData](functions/decodeAttestationData.md)
- [decodeUabPayload](functions/decodeUabPayload.md)
- [deriveKeysFromSignature](functions/deriveKeysFromSignature.md)
- [encodeAttestationData](functions/encodeAttestationData.md)
- [encodeUabPayload](functions/encodeUabPayload.md)
- [encodeV2AttestationMetadata](functions/encodeV2AttestationMetadata.md)
- [ephemeralPrivateKeyToCompressedPublicKey](functions/ephemeralPrivateKeyToCompressedPublicKey.md)
- [externalNullifierFromScope](functions/externalNullifierFromScope.md)
- [extractMetaAddressFromDidDocument](functions/extractMetaAddressFromDidDocument.md)
- [fetchVaa](functions/fetchVaa.md)
- [fieldDefsToString](functions/fieldDefsToString.md)
- [generateRandomMetaAddress](functions/generateRandomMetaAddress.md)
- [getChainDeployment](functions/getChainDeployment.md)
- [getSolanaDeployment](functions/getSolanaDeployment.md)
- [getSupportedChainIds](functions/getSupportedChainIds.md)
- [getUabDeployment](functions/getUabDeployment.md)
- [indexerAnnouncementsToScannerJson](functions/indexerAnnouncementsToScannerJson.md)
- [indexerAnnouncementToScannerRecord](functions/indexerAnnouncementToScannerRecord.md)
- [ipfsPathFromInput](functions/ipfsPathFromInput.md)
- [isZeroUid](functions/isZeroUid.md)
- [keysToStealthMetaAddress](functions/keysToStealthMetaAddress.md)
- [packSchemaIdToField](functions/packSchemaIdToField.md)
- [parseFieldDefs](functions/parseFieldDefs.md)
- [parseMetaAddressValue](functions/parseMetaAddressValue.md)
- [parseStealthMetaAddress](functions/parseStealthMetaAddress.md)
- [randomNonce](functions/randomNonce.md)
- [recomputeStealthSendFromEphemeralPrivateKey](functions/recomputeStealthSendFromEphemeralPrivateKey.md)
- [requestSetupSignature](functions/requestSetupSignature.md)
- [requireChainDeployment](functions/requireChainDeployment.md)
- [requireUabDeployment](functions/requireUabDeployment.md)
- [resolveEnsMetaAddress](functions/resolveEnsMetaAddress.md)
- [resolveIpfsDidMetaAddress](functions/resolveIpfsDidMetaAddress.md)
- [selectSigner](functions/selectSigner.md)
- [stealthMetaAddressToHex](functions/stealthMetaAddressToHex.md)
- [uabPayloadToMetadata](functions/uabPayloadToMetadata.md)
- [uabStealthAddressEvm](functions/uabStealthAddressEvm.md)
