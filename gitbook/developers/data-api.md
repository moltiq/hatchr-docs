---
description: Public Hatchr REST resources for tokens, trades, holders and market state.
---

# Data API

Hatchr's web application reads database-backed REST endpoints for initial state and recovery.

## Endpoints

```text
GET /api/tokens
GET /api/tokens/:address
GET /api/tokens/:address/trades
GET /api/tokens/:address/holders
GET /api/tokens/:address/candles
GET /api/tokens/:address/claimable?creator=0x...
GET /api/tokens/:address/stream
GET /api/search?q=...
GET /api/market/eth-usd
GET /api/chain-stats
GET /api/indexer/health
```

## Data ownership

PostgreSQL is the application source of truth for indexed Hatchr data. Runtime APIs do not silently replace unavailable production data with sample tokens.

## Price data

ETH/USD comes from CoinGecko with a Coinbase fallback and is cached for 60 seconds. Token WETH prices originate from indexed pool state and swaps.

## Availability

The public API is an evolving application interface and is not yet a versioned service-level commitment. Consumers should:

- validate response schemas;
- handle `404`, `429` and `5xx` responses;
- cache immutable token identity fields;
- use transaction hashes and block numbers for deduplication; and
- reconcile important state against chain logs.

{% hint style="warning" %}
Do not place RPC keys, database credentials, Pinata credentials or private keys in browser requests or public repositories.
{% endhint %}

