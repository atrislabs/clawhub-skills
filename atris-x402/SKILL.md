---
name: atris-x402
description: >-
  Call Atris team-1 (checked AI answers), published Atris agents (agent-1),
  AEO visibility audits across ChatGPT & Perplexity, website brand/design
  system extraction, verified PDF-to-Markdown parsing, and YouTube discovery
  using Base Mainnet USDC via x402 v2 with zero API keys and zero signup.
---

# Atris x402 (Zero-API-Key Pay Per Request in Base USDC)

Call 7 live Atris endpoints directly from any x402 v2 wallet (Coinbase Wallet MCP, EIP-3009 signer, or x402 client) on Base Mainnet (`eip155:8453`). No account signup, no API keys, no subscriptions.

## Discovery

- **Well-known manifest:** `https://api.atris.ai/.well-known/x402`
- **OpenAPI 3.1 (`x-payment-info`):** `https://api.atris.ai/x402/openapi.json`
- **Catalog JSON:** `https://api.atris.ai/x402`
- **Live x402scan directory:** `https://www.x402scan.com/server/94aa677d-d793-49c0-8537-a93254c1d552`
- **Runnable Python & Node clients:** `https://github.com/atrislabs/atris-api-examples`

## Endpoints

| Endpoint | Price (Base USDC) | What it does |
|---|---|---|
| `POST https://api.atris.ai/x402/team-1/chat/completions` | `$0.03` | OpenAI-compatible `team-1` (fast open model + stronger reviewer check) |
| `POST https://api.atris.ai/x402/agents/agent-1` | `$0.03` | Published Atris `agent-1` via OpenAI chat completions |
| `POST https://api.atris.ai/x402/aeo/check` | `$0.75` | AI Engine Optimization audit across ChatGPT & Perplexity |
| `POST https://api.atris.ai/x402/design/extract` | `$0.25` | Website brand & CSS design system extraction |
| `POST https://api.atris.ai/x402/design/search` | `$0.05` | Search extracted brand design systems by visual vibe |
| `POST https://api.atris.ai/x402/documents/parse` | `$0.25` | Verified PDF/image to Markdown parser (up to 5 pages) |
| `POST https://api.atris.ai/x402/youtube/search` | `$0.05` | Verified YouTube watch permalinks & titles |

## Payment Flow (x402 v2)

1. Send `POST` to any endpoint above with your JSON body (unpaid).
2. Read the HTTP `402 Payment Required` response and decode the base64 `PAYMENT-REQUIRED` header.
3. Sign an EIP-3009 `TransferWithAuthorization` for Base USDC (`0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913`) to `payTo` and retry with `PAYMENT-SIGNATURE: <base64-payload>`.
4. Receive HTTP `200` with the verified result and onchain settlement hash in `PAYMENT-RESPONSE`. Failed or empty executions are never settled.
