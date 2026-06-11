# Opaque Protocol documentation

This repository is the source of the [Opaque Protocol](https://opaque.cash) documentation site: guides, concepts, and the full `@opaquecash/opaque` SDK reference for stealth payments, provable stealth reputation (PSR), and cross-chain announcements (UAB).

**Live site:** [docs.opaque.cash](https://docs.opaque.cash)

## How publishing works

The site is hosted by [Mintlify](https://mintlify.com) and connected to this repo (`opaquecash/docs`) through the Mintlify GitHub app:

1. Open a branch and edit the MDX pages (or `docs.json` for navigation).
2. Open a pull request. Mintlify posts a preview deployment on the PR so you can review the rendered result before merging.
3. Merge to `main`. Mintlify detects the merge and deploys the new content to the live site automatically, usually within a minute or two.

There is no manual publish step: a merged PR IS the deployment. Anything on `main` is live.

## Local preview

Requires Node.js 20.17+ and the Mintlify CLI:

```bash
npm i -g mint
mint dev
```

Open [http://localhost:3000](http://localhost:3000). The preview hot-reloads as you edit. Run `mint broken-links` before opening a PR to catch dead internal links.

## Repository layout

| Path | Content |
| --- | --- |
| `docs.json` | Mintlify config: navigation, theme, branding |
| `index.mdx` | Landing page |
| `quickstart.mdx` | Five-minute integration walkthrough (`OpaqueClient.fromWallet`) |
| `concepts/` | How the protocol works: stealth payments (CSAP), reputation (PSR), cross-chain (UAB) |
| `guides/` | End-to-end flows: register and receive, send, scan and sweep, schemas, attestations, proofs |
| `sdk/` | Hand-written API reference: `OpaqueClient`, stealth/PSR/reputation/cross-chain APIs, `@opaquecash/react` hooks, utilities |
| `sdk/api/` | Generated TypeDoc reference (never edit by hand) |
| `protocol/` | Protocol overview, spec links, and the deployed contract/program addresses |
| `AGENTS.md` | Writing conventions for contributors and coding agents |

## Generated API reference

`sdk/api/` is emitted by TypeDoc from the SDK source in [`opaquecash/sdk`](https://github.com/opaquecash/sdk). Regenerate it there after SDK releases and commit the result here:

```bash
# in the sdk repo
npm run build && npm run docs:api
```

It is intentionally not wired into the site navigation; the hand-written pages under `sdk/` are the curated reference, and `sdk/api/` serves as the exhaustive raw listing.

## Keeping docs accurate

- Code samples must compile against the current `@opaquecash/opaque` API. When a client method changes in the SDK, update the matching page under `sdk/` and any guide that calls it in the same PR cycle.
- Addresses in `protocol/deployments.mdx` must match the generated `@opaquecash/deployments` package (refreshed via `npm run generate` in the `ethereum/infra` and `solana` repos).
- Style: active voice, second person, no em dashes (use commas, colons, parentheses, or separate sentences). Full conventions live in [`AGENTS.md`](AGENTS.md).

## Related repositories

| Repo | Role |
| --- | --- |
| [`opaquecash/sdk`](https://github.com/opaquecash/sdk) | TypeScript SDK (`@opaquecash/*` packages) the docs describe |
| [`opaquecash/spec`](https://github.com/opaquecash/spec) | Protocol specifications (CSAP, PSR, UAB, payload format) |
| [`opaquecash/ethereum`](https://github.com/opaquecash/ethereum) | EVM contracts |
| [`opaquecash/solana`](https://github.com/opaquecash/solana) | Solana programs |
| [`opaquecash/scanner`](https://github.com/opaquecash/scanner) | Rust cryptography crate (WASM scanner + universal scanner) |

## Support

Questions or corrections: open an issue or PR here, or email [hello@collinsadi.xyz](mailto:hello@collinsadi.xyz).
