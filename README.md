# Opaque documentation

Documentation for [Opaque Protocol](https://opaque.cash), built with [Mintlify](https://mintlify.com).

**Live site:** Connect this repo (`opaquecash/mintlify-docs`) in the Mintlify dashboard and set custom domain `docs.opaque.cash`.

## Local preview

Requires Node.js 20.17+.

```bash
npm i -g mint
cd docs && mint dev
```

Open [http://localhost:3000](http://localhost:3000).

## Structure

| Path | Content |
| --- | --- |
| `docs.json` | Navigation, branding, navbar |
| `index.mdx` | Welcome |
| `quickstart.mdx` | 5-minute integration |
| `concepts/` | CSAP, PSR, UAB |
| `guides/` | End-to-end flows |
| `sdk/` | `OpaqueClient` API reference |
| `protocol/` | Spec links and deployments |

## Publishing

Push to `main` on `opaquecash/mintlify-docs`. Mintlify auto-deploys when the GitHub app is connected.

## SDK source

API docs reflect `@opaquecash/opaque` in [`opaquecash/sdk`](https://github.com/opaquecash/sdk). Update docs when client methods change.
