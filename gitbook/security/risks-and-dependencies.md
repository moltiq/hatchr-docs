---
description: Market, smart-contract, infrastructure and metadata risks.
---

# Risks and Dependencies

Using Hatchr involves smart-contract, market and infrastructure risk.

## Market risk

- New tokens can be extremely volatile.
- Implied market cap is not redeemable backing.
- Concentrated liquidity can produce significant price impact.
- Low WETH depth can make exits expensive or impossible at an expected price.
- Graduation does not guarantee value, liquidity or future activity.

## Smart-contract risk

- Hatchr has not yet published an independent audit.
- Uniswap V3 and Robinhood Chain contracts are external dependencies.
- Wallet simulation and scanners may miss vulnerabilities.
- A successful transaction is not proof that a token is economically safe.

## Infrastructure risk

The application depends on:

- Robinhood Chain and its RPC infrastructure;
- Uniswap V3 deployments;
- Blockscout historical APIs;
- PostgreSQL, Railway and Vercel;
- public IPFS gateways and Pinata;
- CoinGecko and Coinbase price APIs; and
- Dexscreener for embedded charts.

Frontend or indexer downtime does not disable direct Uniswap pool trading, but it can delay discovery, analytics, metadata and fee displays.

## Metadata and social risk

Creators control token metadata and community links. Hatchr's technical launch does not endorse a creator, roadmap, website or social account.

## Reorganization and indexing risk

Hatchr uses a confirmation buffer, but deep chain reorganizations or provider failures can temporarily produce stale application state. Verify important events against the chain.

{% hint style="danger" %}
Nothing in these docs is financial, legal or investment advice. Never spend funds you cannot afford to lose.
{% endhint %}

